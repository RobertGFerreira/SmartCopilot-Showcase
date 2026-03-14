<div align="center">

# <img src="assets/smartcopilot_icon.png" alt="Icon" width="40" height="40" style="vertical-align: middle;"> SmartCopilot Platform (Showcase)

### *Ecossistema de Otimização Dinâmica para Motoristas de Aplicativo*

<p>
  Uma solução <b>Natívio-Híbrida Full-Stack</b> que integra Serviços de Acessibilidade nativa Android, Visão Computacional (OCR) <br>
  e um robusto Backend Inteligente para transformar dados de corridas em ganhos reais em tempo real.
</p>

<!-- Badges Unificadas Front + Back -->
<p>
  <img src="https://img.shields.io/badge/Frontend-Flutter_3.x-02569B?style=for-the-badge&logo=flutter&logoColor=white" alt="Flutter" />
  <img src="https://img.shields.io/badge/Native_Core-Kotlin_&_Java-7F52FF?style=for-the-badge&logo=kotlin&logoColor=white" alt="Kotlin" />
  <img src="https://img.shields.io/badge/OCR-ML_Kit-4285F4?style=for-the-badge&logo=google&logoColor=white" alt="ML Kit" />
  <img src="https://img.shields.io/badge/Backend-Supabase_&_PostgreSQL-3ECF8E?style=for-the-badge&logo=supabase&logoColor=white" alt="Supabase Backend" />
</p>

<br>

<!-- Links do Projeto -->
<a href="https://play.google.com/store/apps/details?id=com.smartcopilot.app&hl=pt_BR" target="_blank">
  <img src="https://img.shields.io/badge/Google_Play-Baixar_App-414141?style=for-the-badge&logo=googleplay&logoColor=white" alt="Google Play">
</a>
<a href="https://btectech.github.io/smartcopilot-site/" target="_blank">
  <img src="https://img.shields.io/badge/Website-Oficial-000000?style=for-the-badge&logo=vercel&logoColor=white" alt="Website Oficial">
</a>

</div>

---

## 📖 Sobre o Projeto

Este repositório serve como **Vitrine Técnica (Showcase)** para o **SmartCopilot**, um software proprietário desenvolvido para automatizar a tomada de decisão para motoristas de aplicativos (Uber, 99, Indrive).

O sistema resolve a assimetria de informações enfrentada pelos motoristas na rua, interceptando cards de corrida em microssegundos (via Android Accessibility Services) e fornecendo análises precisas (R$/km, R$/hora, Zonas de Risco) numa interface **Flutter (Material 3)** flutuante e hiper-otimizada.

> ⚠️ **Nota:** *O código-fonte completo é privado. Este repositório demonstra a arquitetura, funcionalidades, stack tecnológica e o roadmap de desenvolvimento.*

---

## 📸 Visão Geral da Interface

<div align="center">
  <!-- SUBSTITUA POR SEUS PRINTS REAIS NA PASTA ASSETS -->
  <img src="assets/dashboard_preview.png" alt="Interface Flutuante (Overlay) do SmartCopilot" width="100%" style="border-radius: 10px; margin-bottom: 20px;">
  <br>
  <em>Dashboard de controle e overlay inteligente analisando uma corrida em tempo real.</em>
</div>

---

## 🆕 Capacidades Recentes & Inovações

A arquitetura do SmartCopilot foi desenhada para operação **Zero-Latency/Offline-First**, garantindo que as avaliações de corrida ocorram localmente em milissegundos.

### ⚙️ Engenharia Nativa Android (Kotlin)
*   **Accessibility Service Profundo:** Monitoramento contínuo da árvore de elementos (DOM nativo) de aplicativos de transporte para extrair dados sem afetar a performance do device.
*   **Overlay Engine Avançado:** Renderização de janelas sobrepostas (System Alert Window) que reagem dinamicamente à tela de fundo.
*   **Gerenciamento de Energia & Background:** Serviços estabilizados (Foreground Services, Wakelocks) desenhados para não serem "mortos" pelas baterias agressivas das OEMs (Xiaomi, Samsung).
*   **Fallback Inteligente via ML (OCR):** Quando a árvore de acessibilidade é ofuscada pelas plataformas, o sistema captura a tela e a submete a extração óptica via Google ML Kit On-Device.

### 🎨 Frontend & App Arquitetura (Flutter)
*   **Motor de Filtros de Alta Performance:** Avaliação instantânea (R$/km, HR) de cada corrida contra dezenas de filtros definidos pelo usuário (Destinos Indesejados, Limite Mínimo, Nota do Passageiro).
*   **Design System Material 3:** Interface limpa, responsiva e com feedback tátil.
*   **Modularização Baseada em Features:** Clean Architecture aplicada ao Dart, separando *Core*, *Features* e *Services* para manutenção escalonável.
*   **Gestão de Estado Reativa:** Integração sem atrito com o Kotlin Bridge para comunicar a detecção de chamadas diretamente aos Controllers Dart.

### 🧠 Backend, Analytics & Freemium Edge
*   **Assinaturas e Controle de Tempo:** Motor distribuído de controle "Freemium" que provisiona horas de funcionamento para testes controlados via Supabase Edge Functions.
*   **Metrificação (TimeBankController):** Monitoramento persistente de sessões e engajamento.

---

## 🛡️ Destaques Técnicos & Segurança

### Nativo & Dart
*   **Integração Plataforma Completa:** Uso avançado de *MethodChannels* e *EventChannels* para bidirecionalidade assíncrona.
*   **Isolates & Background:** Tarefas pesadas (ex. Parsing de Corridas complexas via Expressões Regulares) rodando fora da UI-Thread (Main Isolate).
*   **Resiliência a Ofuscação:** Parsers projetados para reagir a variações e Testes A/B na interface do Uber e 99.

---

## 🚀 Roadmap e Próximos Passos

O desenvolvimento atual foca na maturidade de Automação para os motoristas, evoluindo de uma ferramenta analítica para uma "Mão Auxiliar".

### 🚗 Automação de Corridas 
- [ ] **Macro Actions (Auto-Aceite):** Comando nativo de clique programático (`ACTION_CLICK`) para aceitar instantaneamente corridas que atinjam nota 10/10 no algoritmo.
- [ ] **Auto-Recusa Inteligente:** Fechar e dispensar chamadas péssimas, limpando a tela para aumentar a segurança viária do motorista.
- [ ] **Expansão de Parsers:** Aumento de precisão OCR para modelos de aparelhos específicos.

### 🔐 Plataforma & Monetização
- [ ] **Gateway de Pagamento Integrado:** Subscrições in-app habilitadas de forma orgânica.
- [ ] **Fleet Analytics:** Dashboard remoto via Web (React/Flutter Web) para frotistas que quiserem alugar o sistema.

---

## 🏗️ Arquitetura de Alto Nível (System Design)

Abaixo, a representação simplificada do fluxo de dados e dos módulos do sistema, desenhada para ilustrar a interação entre o Flutter, o Core Nativo do Android e o Backend Serverless, sem expor a lógica restrita.

```mermaid
graph TD
    subgraph Frontend [Flutter Front-End]
        UI[Material 3 UI Settings]
        Dart[Dart Engine & Pipeline]
    end

    subgraph Native [Android Native Core]
        ACC[Accessibility Service]
        Overlay[System Alert Window]
        ML[ML Kit On-Device]
    end

    subgraph Backend [Backend & Cloud]
        Edge[Supabase Edge Functions]
        DB[(PostgreSQL TimeBank)]
        Storage[Offline Storage SQLite]
    end

    ACC --"Extracts Screen Data (µs)"--> Dart
    Dart --"Renders Ride Overlay"--> Overlay
    ML --"Fallback OCR (ms)"--> Dart
    Dart --"Persists Offline"--> Storage
    Storage --"Syncs Freemium Session"--> Edge
    Edge <--> DB
```

---

## 🛠️ Stack Tecnológica Completa

<div align="center">

| Categoria | Tecnologias Principais | Detalhes |
| :--- | :--- | :--- |
| **Cross-Platform** | **Flutter** | Material 3, MethodChannels, Dart 3 |
| **Core Nativo** | **Kotlin / Java** | Android AccessibilityService, Overlay Services, ML Kit |
| **Local Storage** | **SharedPrefs/SQLite** | Persistência ultra-rápida offline-first |
| **Backend & Gen** | **Supabase** | Edge Functions, PostgreSQL remote |

</div>

---

## 📚 Documentação Técnica Aprofundada

Para explorar mais a fundo a arquitetura e as soluções de engenharia do SmartCopilot, consulte os documentos abaixo:

- [Diferenciais Técnicos](docs/diferenciais.md): Detalhes sobre a arquitetura híbrida, overlay nativo e resiliência offline.
- [Ferramentas Utilizadas](docs/ferramentas.md): Ecossistema de desenvolvimento, DevOps, QA e Analytics.
- [Tecnologias do Sistema](docs/tecnologias.md): Stack detalhada do aplicativo (Dart/Kotlin) e backend (Supabase).

---

## 📄 Licença e Termos de Uso

Este é um software **proprietário**. O código-fonte principal é restrito aos desenvolvedores e proprietários do projeto. Este repositório destina-se apenas a portfólio e demonstração de arquitetura.

- **Status do App:** Atualmente em fase de Testes Fechados na Google Play Store. O link da loja será substituído quando o lançamento oficial ocorrer.
- **Termos e Condições:** A cópia, distribuição não autorizada, comercialização ou engenharia reversa do código-fonte ou dos binários do SmartCopilot é estritamente proibida e passível de medidas legais. O uso do aplicativo está sujeito aos termos aceitos no momento do cadastro.

---

<div align="center">

## 👨💻 Suporte & Contato

**Suporte Oficial do App:**
<br>
<a href="mailto:contato.smartcopilot@gmail.com" target="_blank">
  <img src="https://img.shields.io/badge/E--mail_Suporte-contato.smartcopilot%40gmail.com-D14836?style=for-the-badge&logo=Gmail&logoColor=white" alt="E-mail de Suporte">
</a>

<br><br>

**Robert Ferreira (Desenvolvedor)**
<br>
*Engenheiro de Software Full-Stack | Especialista em Mobile Nativo & Cross-Platform*

<br>

<a href="https://www.linkedin.com/in/robert-guilherme-ferreira/" target="_blank">
  <img src="https://img.shields.io/badge/-LinkedIn-0077B5?style=for-the-badge&logo=Linkedin&logoColor=white" alt="LinkedIn">
</a>
<a href="mailto:contato.robferreira@gmail.com" target="_blank">
  <img src="https://img.shields.io/badge/-Gmail-D14836?style=for-the-badge&logo=Gmail&logoColor=white" alt="Gmail">
</a>
<a href="https://github.com/RobertGFerreira" target="_blank">
  <img src="https://img.shields.io/badge/-Portfolio-181717?style=for-the-badge&logo=github&logoColor=white" alt="GitHub">
</a>

<br><br>
<sub>© 2026 Robert Ferreira. Todos os direitos reservados.</sub>

</div>
