# Ferramentas Utilizadas no SmartCopilot

Este documento detalha o ecossistema de ferramentas de desenvolvimento, DevOps e monitoramento empregadas no sistema **SmartCopilot**.

## Desenvolvimento e Codificação

- **Git & GitHub**: Plataforma mandatória para hospedagem remota, revisão e versionamento de branches para novas automações.
- **VS Code & Android Studio**: IDEs complementares. VS Code domina a codificação em Dart/Flutter enquanto o Android Studio viabiliza o debugging detalhado do Kotlin (`AccessibilityService`) e do Manifest Android.
- **Firebase Console**: Utilizado na fase de acompanhamento de banco de dados NoSQL (Firestore) e logs de autenticação.

## DevOps, CI/CD e Background

- **Flutter/Dart CLI**: Build automation do APK e extração de blocos (`build appbundle`).
- **Firebase CLI**: Implantação de regras de segurança do Firestore e (futuramente) Cloud Functions.
- **ProGuard / R8**: Ofuscação ativa das camadas nativas durante builds de release para prevenção de detecção pelos aplicativos de mobilidade urbana.

## Testes e Qualidade

- **Flutter Test**: Pipeline de assertividade do *State Management* (Provider/Controllers) para regras lógicas do Freemium e permissões de usuários.
- **ADB (Android Debug Bridge)**: Utilidade extrema para injeção via command-line e depuração de Window Layers (Overlays).

## Analytics e Backoffice Local

- **SharedPreferences Inspector**: Ferramentas de debug do Flutter para validação offline-first antes da sincronização remota.
- **Firebase Crashlytics / Analytics**: Previsão de tracking de falhas no app e uso do sistema.

Essas ferramentas sustentam a confiabilidade técnica da solução em um ambiente tão dinâmico como o dia-a-dia logístico.
