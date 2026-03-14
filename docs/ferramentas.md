# Ferramentas Utilizadas no SmartCopilot

Este documento detalha o ecossistema de ferramentas de desenvolvimento, DevOps e monitoramento empregadas no sistema **SmartCopilot**.

## Desenvolvimento e Codificação

- **Git & GitHub**: Plataforma mandatória para hospedagem remota, revisão e versionamento de branches para novas automações.
- **VS Code & Android Studio**: IDEs complementares. VS Code domina a codificação em Dart/Flutter enquanto o Android Studio viabiliza o debugging detalhado do Kotlin (`AccessibilityService`) e do Manifest Android.
- **DBeaver & Prisma Studio**: Utilizadas na fase de rascunhos de esquemas de banco antes de consolidá-los via migrations ou interface do Supabase.

## DevOps, CI/CD e Background

- **Flutter/Dart CLI**: Build automation do APK e extração de blocos (`build appbundle`).
- **Supabase CLI**: Edge Functions testing, pushing e sincronização remota do banco de dados (PostgreSQL).
- **ProGuard / R8**: Ofuscação ativa das camadas nativas durante builds de release para prevenção de detecção pelos aplicativos de mobilidade urbana.

## Testes e Qualidade

- **Flutter Test**: Pipeline de assertividade do *State Management* (Provider/Controllers) para regras lógicas do Freemium e permissões de usuários.
- **ADB (Android Debug Bridge)**: Utilidade extrema para injeção via command-line e depuração de Window Layers (Overlays).

## Analytics e Backoffice Local

- **SQLite Inspector**: Validação offline-first dos históricos locais antes da sincronização remota.
- **Supabase Logs**: Stream ao vivo de invocação de Edge Functions, rastreando falhas nos limites de requisição de motoristas em teste.

Essas ferramentas sustentam a confiabilidade técnica da solução em um ambiente tão dinâmico como o dia-a-dia logístico.
