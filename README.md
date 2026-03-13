🚗 SmartCopilot Platform (Showcase)

Ecossistema Inteligente de Gestão Financeira para Mobilidade

📖 Sobre o Projeto

Este repositório serve como Vitrine Técnica (Showcase) para o SmartCopilot, um software mobile proprietário desenvolvido para resolver a assimetria de informações no ecossistema de motoristas de aplicativo (Uber, 99, etc).

O sistema resolve a falta de transparência operacional. Em média, um motorista tem 5 segundos para aceitar ou recusar uma corrida sem saber o lucro real. O SmartCopilot atua como um motor invisível, usando Visão Computacional (OCR) via Android Accessibility API para ler a oferta, cruzar com os custos operacionais do veículo e exibir um HUD (Overlay) inteligente para a tomada de decisão.

⚠️ Nota: O código-fonte completo é proprietário e fechado. Este repositório demonstra as decisões arquiteturais, o design de sistema, a stack tecnológica e o roadmap de desenvolvimento.

📸 Visão Geral da Interface

🆕 Changelog: Atualização Recente (v1.0 - MVP)

A atualização de pré-lançamento focou em Estabilidade de Background, Gestão de Estado Reativa e Separação de Privilégios (RBAC).

🧠 Arquitetura Nativa e Processamento

OCR Heurístico Tolerante a Falhas: Novo motor de parsing que não depende de layouts fixos, capaz de ler textos fragmentados de ofertas complexas (viagens múltiplas, VIP, etc).

Isolamento de Background: Implementação de Foreground Services (flutter_background_service) com wakelocks para garantir a sobrevivência do leitor durante horas de uso intenso com a tela desligada.

Whitelisting Dinâmico: O motor de OCR agora "hiberna" ativamente se o aplicativo em foco não for um dos apps de mobilidade mapeados, resultando em economia drástica de CPU e Bateria.

🎨 Frontend & Gestão de Estado

Design System Premium: Padronização visual completa focada em Dark Mode de alto contraste, ideal para uso noturno e automotivo.

Feature Flags & Whitelist: Sistema de injeção de dependências via Riverpod que gerencia os planos (Free vs Premium) em tempo real, com bypass administrativo em runtime para os desenvolvedores.

Laboratório de Testes Offline (Mocking): Criação de um ambiente de DevTools interno que permite injetar imagens da galeria e simular payloads do OCR sem necessitar de corridas reais.

🛡️ Destaques Técnicos & Compliance

Integração Nativa (Kotlin ↔ Flutter)

System Alert Window: Renderização de UI complexa (Flutter) sobreposta a outros aplicativos (System Overlay).

MethodChannels: Comunicação assíncrona bidirecional de alta performance. O Android captura o nó de acessibilidade e o repassa instantaneamente ao Dart para orquestração da regra de negócio.

Segurança e Política de Uso (Play Store Compliance)

Zero GPS: Para garantir privacidade e economizar hardware, a aplicação depende estritamente da tela e do contexto, não consumindo requisições de geolocalização em background.

Gestão Local: Dados sensíveis de viagens, ganhos e prints de auditoria são persistidos offline no dispositivo (Isar DB), respeitando políticas restritas de privacidade.

🚀 Roadmap e Próximos Passos

A evolução foca na transição de uma ferramenta de "cálculo" para uma suíte de "Automação e Previsibilidade".

📊 Dados e Inteligência

[ ] Mapeamento de Áreas de Risco (Offline): Estrutura GeoJSON local para cruzar os endereços lidos na tela com zonas críticas, gerando alertas no HUD antes do aceite.

[ ] Detecção de Estado da Viagem: Refinamento do leitor para identificar não apenas a oferta, mas o ciclo de vida completo (Em andamento, Finalizada, Cancelada).

[ ] Dashboards Avançados: Filtros de exportação de dados para contabilidade de impostos e depreciação real da frota.

🔐 Escala SaaS

[ ] Integração RevenueCat: Gestão de entitlements e controle de assinaturas cross-platform.

[ ] Sincronização Cloud: Backup opt-in via Firebase para proteção de auditoria (comprovantes de retenção de valores das plataformas).

🛠️ Stack Tecnológica Completa

Categoria

Tecnologias Principais

Detalhes

Mobile Frontend

Flutter 3.x

Riverpod (State), Google Fonts, System Overlay

Mobile Native

Kotlin / Android

AccessibilityService API, Wakelock, MethodChannels

Processamento (AI/ML)

Google ML Kit

Text Recognition V2, Regex Pattern Matching

Banco de Dados

Isar Database

NoSQL de altíssima velocidade, queries assíncronas

Infra & Monetização

Firebase / AdMob

Auth Offline-first, Rewarded Video Ads

🤝 Direitos Autorais

Este é um software proprietário. O código-fonte e a propriedade intelectual pertencem exclusivamente ao seu autor. Este repositório público destina-se apenas à demonstração de capacidades técnicas de engenharia de software e portfólio.

👨‍💻 Autor & Contato

Robert Ferreira





Engenheiro de Software Mobile | Especialista em Flutter & Integrações Nativas






© 2026 SmartCopilot. Todos os direitos reservados.