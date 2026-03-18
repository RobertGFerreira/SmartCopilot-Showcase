# Ferramentas Utilizadas no SmartCopilot

Este documento detalha o ecossistema de ferramentas de desenvolvimento, DevOps e monitoramento empregadas no sistema **SmartCopilot**.

## Desenvolvimento e Codificação

- **Git & GitHub:** Plataforma de hospedagem remota, revisão de código e versionamento de branches para novas features e automações.
- **VS Code & Android Studio:** IDEs complementares. VS Code domina a codificação em Dart/Flutter com extensões de Riverpod e análise estática; Android Studio viabiliza o debugging detalhado do Kotlin (`AccessibilityService`) e inspeção do Manifest Android.
- **Firebase Console:** Acompanhamento do banco de dados Firestore, autenticação de usuários e logs de erro em tempo real.

## DevOps, Build e Geração de Código

- **Flutter/Dart CLI:** Build automation do APK (`flutter build apk`) e bundle de release (`flutter build appbundle`).
- **build_runner:** Geração de código automática para os schemas do Isar (`*.g.dart`) e demais anotações — parte do pipeline de compilação para cada novo modelo de dados.
- **Firebase CLI:** Implantação de regras de segurança do Firestore e (futuramente) Cloud Functions.
- **ProGuard / R8:** Ofuscação ativa das camadas nativas durante builds de release para redução de superfície de detecção pelos aplicativos de mobilidade urbana.

## Testes e Qualidade

- **Flutter Test:** Pipeline de assertividade do gerenciamento de estado (Riverpod Controllers) para regras lógicas do Freemium, parsers de corrida e permissões de usuários.
- **Flutter Analyze:** Análise estática com zero warnings como padrão — `RegExp` apenas como `static final`, null-safety rigoroso e `if (!mounted)` em todos os gaps assíncronos com `BuildContext`.
- **ADB (Android Debug Bridge):** Depuração de Window Layers (Overlays), injeção de eventos de acessibilidade e inspeção de permissões especiais via command-line.

## Inspeção e Debug

- **Isar Inspector:** Interface web integrada ao Isar para inspeção das collections em tempo real durante o desenvolvimento — histórico de corridas, configurações e fila WAL de operações pendentes.
- **SharedPreferences Inspector:** Validação offline-first de flags e estado de sessão antes da sincronização remota.
- **Firebase Crashlytics / Analytics:** Tracking de falhas em produção e métricas de uso do sistema.

## Qualidade de Código — Padrões Adotados

- **Zero `print()` em produção:** Logs verbosos de debug guardados por `kDebugMode`
- **Lint customizado:** Regras de análise estática para garantir isolamento dos parsers, uso correto de `copyWith` nos controllers de overlay e ausência de mutação cruzada entre providers
- **Cobertura de mounted guards:** `if (!mounted) return` obrigatório em todos os métodos `async` que usam `BuildContext` após um `await`

Essas ferramentas sustentam a confiabilidade técnica da solução em um ambiente tão dinâmico como o dia a dia logístico dos motoristas.
