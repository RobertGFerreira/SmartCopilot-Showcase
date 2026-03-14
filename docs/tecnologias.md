# Tecnologias do SmartCopilot

O Stack Tecnológico do SmartCopilot foi orquestrado para suportar avaliações assíncronas hiper-rápidas, e persistência robusta local, garantindo não interferência no tráfego de dados sensíveis da corrida real.

## Core Multi-Plataforma

- **Dart (Flutter 3.x)**: O grande cérebro do UI e estado da aplicação principal, provendo a fluidez de 60/120Hz aos Floating Widgets (M3) e o ciclo de filtragem de motoristas (calculadoras de Reais por Quilômetros e Reais por Hora).

## Core Android Nativo

- **Kotlin / Java**: Essenciais para acesso subjacente em domínios não cobertos facilmente por plataformas híbridas.
  - *Accessibility Services*: Acessado em Kotlin nativamente para serialização rápida da tela e envio na *Bridge*.
  - *System Alert Window*: Camada responsável pelo "desenho" físico da janela do flutter acima dos demais aplicativos do sistema android de forma nativa.
  - *Foreground Services*: Estabilização técnica e uso pontual de Battery Wakelocks em Kotlin.

## Backend e Banco de Dados

- **Supabase (Backend-as-a-Service)**: Nuvem unificada baseada no pacote *Open Source*.
  - **PostgreSQL**: Sólido gerenciamento na nuvem para manter contas autorizadas e rastrear tempos consumidos em abas freemium (TimeBank).
  - **Supabase Edge Functions**: Rotinas serverless acionadas pelos celulares esparsos para computar encerramentos/sincronizações.
- **SQLite / SharedPreferences**: Local Storage. Permite que o "Parser" analise um card de viagem mesmo se o motorista rodar em "Sombra Urbana" com rede H+ ou 3G caindo, e depois suba isso ao repo online.

## Bibliotecas e Serviços Especializados

- **Google ML Kit (Visão Computacional)**: Integração nativa de modelos robustos *On-Device Text Recognition*, permitindo ao Dart processar prints passados por bytearray do Kotlin numa segunda camada de resiliência.
- **Provider (Gerência de Estado)**: Injeção de dependências e escuta de Models centralizados.
- **Permission Handler**: Componente de front para manusear as elevadas restrições (Permissões Especiais) do Android moderno que o app demanda.
