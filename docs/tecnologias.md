# Tecnologias do SmartCopilot

O stack tecnológico do SmartCopilot foi orquestrado para suportar avaliações assíncronas em microssegundos e persistência robusta local, garantindo operação completa mesmo sem conectividade de rede.

## Core Multi-Plataforma

- **Dart (Flutter 3.x):** O motor do UI e estado da aplicação. Provê fluidez de 60/120Hz nos Floating Widgets (Material 3) e o ciclo completo de avaliação de corridas — cálculo de R$/km, R$/hora, semáforo de rentabilidade e filtros de destino.

## Core Android Nativo

- **Kotlin:** Essencial para acesso a domínios não cobertos por plataformas híbridas.
  - *Accessibility Services:* Monitoramento da árvore de elementos dos apps de transporte com lookup de pacote em O(1) via `HashSet`.
  - *System Alert Window:* Camada responsável pelo desenho físico da janela Flutter acima dos demais apps do sistema Android.
  - *Foreground Services + Wakelock:* Estabilização técnica para operação contínua durante plantões longos, resistente ao kill de OEMs agressivas (Xiaomi, Samsung, Motorola).

## Banco de Dados Local

- **Isar:** Banco de dados NoSQL local de alta performance. Utilizado para persistir histórico de corridas, configurações do overlay, parâmetros do semáforo e a fila de operações pendentes do Write-Ahead Log (WAL).
- **SharedPreferences:** Persistência ultra-rápida de estado de sessão, posição do overlay na tela e flags de onboarding — ideal para leituras síncronas na inicialização.

## Backend e Nuvem

- **Firebase (Backend-as-a-Service):**
  - **Cloud Firestore:** Banco de dados NoSQL para contas autorizadas, controle de sessões freemium (TimeBank) e histórico de corridas sincronizado.
  - **Firebase Auth:** Autenticação com suporte a Google Sign-In e grace period offline.
  - **Firebase Cloud Functions:** *(Planejado)* Rotinas serverless para validação de sessões e sincronizações avançadas.

## Gerência de Estado

- **Riverpod:** Injeção de dependências e gerência de estado reativa. Providers desacoplados com comunicação via `Stream` entre `StateNotifier` — elimina mutação direta entre providers e torna o fluxo de dados previsível e testável.

## Bibliotecas Especializadas

- **Google ML Kit (Visão Computacional):** Modelos de *On-Device Text Recognition* para extração ótica de dados das telas dos apps de transporte. Roda 100% local — zero envio de imagem para servidores externos.
- **flutter_overlay_window:** Gerenciamento da janela flutuante do overlay sobre outros apps.
- **flutter_background_service:** Manutenção do serviço de monitoramento em background com proteção anti-kill.
- **Permission Handler:** Componente de front para gerenciar as permissões especiais que o app demanda no Android moderno (Accessibility, Overlay, Background).
