<!DOCTYPE html>
<html lang="pt-BR">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>AgroIntelligence Platform - Showcase</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <style>
        /* Custom scrollbar para um visual mais limpo */
        ::-webkit-scrollbar {
            width: 8px;
        }
        ::-webkit-scrollbar-track {
            background: #0f172a; 
        }
        ::-webkit-scrollbar-thumb {
            background: #334155; 
            border-radius: 4px;
        }
        ::-webkit-scrollbar-thumb:hover {
            background: #475569; 
        }
        body {
            font-family: -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, Helvetica, Arial, sans-serif;
        }
    </style>
</head>
<body class="bg-slate-950 text-slate-300 antialiased leading-relaxed selection:bg-emerald-500 selection:text-white">

    <div class="max-w-5xl mx-auto px-6 py-16">
        
        <!-- Header Section -->
        <header class="text-center mb-16">
            <h1 class="text-4xl md:text-5xl font-extrabold text-white mb-4 tracking-tight">
                🌾 AgroIntelligence Platform <span class="text-emerald-400 font-light text-3xl md:text-4xl">(Showcase)</span>
            </h1>
            <h3 class="text-xl md:text-2xl text-slate-400 italic font-light mb-6">Ecossistema de Gestão Agrícola Digital & Inteligência Artificial</h3>
            
            <p class="text-lg text-slate-300 max-w-3xl mx-auto mb-8 leading-relaxed">
                Uma solução <b class="text-white">Full-Stack Enterprise</b> que integra IoT, Visão Computacional e LLMs <br class="hidden md:block">
                para transformar dados brutos do campo em decisões agronômicas precisas.
            </p>

            <!-- Badges -->
            <div class="flex flex-wrap justify-center gap-3 mb-8">
                <img src="https://img.shields.io/badge/Frontend-Flutter_3.x-02569B?style=for-the-badge&logo=flutter&logoColor=white" alt="Flutter" class="h-8 rounded shadow-sm hover:scale-105 transition-transform">
                <img src="https://img.shields.io/badge/Backend-Python_3.13-3776AB?style=for-the-badge&logo=python&logoColor=white" alt="Python" class="h-8 rounded shadow-sm hover:scale-105 transition-transform">
                <img src="https://img.shields.io/badge/API-FastAPI-009688?style=for-the-badge&logo=fastapi&logoColor=white" alt="FastAPI" class="h-8 rounded shadow-sm hover:scale-105 transition-transform">
                <img src="https://img.shields.io/badge/AI-Ollama_RAG-000000?style=for-the-badge&logo=ollama&logoColor=white" alt="AI RAG" class="h-8 rounded shadow-sm hover:scale-105 transition-transform">
                <img src="https://img.shields.io/badge/Database-PostgreSQL-4169E1?style=for-the-badge&logo=postgresql&logoColor=white" alt="PostgreSQL" class="h-8 rounded shadow-sm hover:scale-105 transition-transform">
            </div>

            <a href="https://www.linkedin.com/in/robert-guilherme-ferreira/" target="_blank" class="inline-block hover:scale-105 transition-transform">
                <img src="https://img.shields.io/badge/Solicitar_Demo_Técnica-0077B5?style=for-the-badge&logo=linkedin&logoColor=white" alt="Solicitar Demo" class="h-10 rounded shadow-lg shadow-blue-900/20">
            </a>
        </header>

        <!-- Sobre o Projeto -->
        <section class="mb-16">
            <h2 class="text-2xl md:text-3xl font-bold text-white mb-6 border-b border-slate-800 pb-3 flex items-center gap-3">
                <span class="text-emerald-500">📖</span> Sobre o Projeto
            </h2>
            <div class="space-y-4">
                <p>Este repositório serve como <strong>Vitrine Técnica (Showcase)</strong> para o <strong>Sistema Agrícola</strong>, um software proprietário desenvolvido para digitalizar operações rurais de ponta a ponta.</p>
                <p>O sistema resolve a fragmentação tecnológica no campo, unificando gestão de inventário, monitoramento meteorológico e agronomia em uma interface <strong>Flutter (Material 3)</strong> moderna, alimentada por um backend <strong>Python/FastAPI</strong> robusto que utiliza <strong>IA Generativa (RAG)</strong> para consultas contextuais complexas.</p>
            </div>
            
            <div class="mt-8 bg-slate-800/50 border-l-4 border-amber-500 p-6 rounded-r-xl">
                <p class="text-amber-100 flex gap-3">
                    <span class="text-xl">⚠️</span>
                    <span><strong>Nota:</strong> O código-fonte completo é privado. Este repositório demonstra a arquitetura, funcionalidades, stack tecnológica e o roadmap de desenvolvimento.</span>
                </p>
            </div>
        </section>

        <!-- Visão Geral -->
        <section class="mb-16 text-center">
            <h2 class="text-2xl md:text-3xl font-bold text-white mb-8 border-b border-slate-800 pb-3 text-left flex items-center gap-3">
                <span class="text-emerald-500">📸</span> Visão Geral da Interface
            </h2>
            
            <div class="flex justify-center items-center">
                <div class="w-full max-w-4xl bg-slate-800 rounded-2xl p-2 border border-slate-700 shadow-xl shadow-black/50 hover:-translate-y-2 transition-transform duration-300">
                    <img src="assets/dashboard_v2.png" alt="Dashboard do Sistema Agrícola em Material 3" class="w-full rounded-xl" onerror="this.src='https://via.placeholder.com/1200x600/1e293b/10b981?text=Dashboard+Agro+V2'">
                    <p class="text-sm text-slate-400 mt-4 pb-3 font-medium">Dashboard responsivo com design system Material 3 e monitoramento em tempo real.</p>
                </div>
            </div>
        </section>

        <!-- Changelog -->
        <section class="mb-16">
            <h2 class="text-2xl md:text-3xl font-bold text-white mb-6 border-b border-slate-800 pb-3 flex items-center gap-3">
                <span class="text-emerald-500">🆕</span> Changelog: Atualização Recente (v2.0)
            </h2>
            <p class="mb-8 text-slate-300">A atualização mais recente focou na <strong>Padronização Enterprise</strong> e na introdução de capacidades avançadas de <strong>IA Generativa Contextual</strong>.</p>

            <div class="grid md:grid-cols-2 gap-8">
                <div class="bg-slate-900 border border-slate-800 p-6 rounded-2xl">
                    <h3 class="text-xl font-bold text-emerald-400 mb-4 flex items-center gap-2">🧠 Backend & IA (Python)</h3>
                    <ul class="space-y-4">
                        <li class="flex gap-3">
                            <span class="text-emerald-500 mt-1">•</span>
                            <span><strong>RAG (Retrieval-Augmented Generation):</strong> O sistema agora "conversa" com o banco de dados. <em>Exemplo: "Que dia vou colher no Talhão 3?"</em> e a IA analisa dados para responder.</span>
                        </li>
                        <li class="flex gap-3">
                            <span class="text-emerald-500 mt-1">•</span>
                            <span><strong>Módulo de Patologia Agrícola:</strong> Importação massiva de +3.000 itens catalogados, incluindo doenças, pragas e ervas daninhas.</span>
                        </li>
                        <li class="flex gap-3">
                            <span class="text-emerald-500 mt-1">•</span>
                            <span><strong>Chatbot Integrado & RBAC:</strong> Assistente virtual nativo para suporte operacional e infraestrutura preparada para gestão de permissões por usuário.</span>
                        </li>
                        <li class="flex gap-3">
                            <span class="text-emerald-500 mt-1">•</span>
                            <span><strong>Automação & Clean Architecture:</strong> Fundação lógica para controle de pivôs via IoT e refatoração completa de Models/Schemas.</span>
                        </li>
                    </ul>
                </div>

                <div class="bg-slate-900 border border-slate-800 p-6 rounded-2xl">
                    <h3 class="text-xl font-bold text-emerald-400 mb-4 flex items-center gap-2">🎨 Frontend & UX (Flutter)</h3>
                    <ul class="space-y-4">
                        <li class="flex gap-3">
                            <span class="text-emerald-500 mt-1">•</span>
                            <span><strong>Design System Material 3:</strong> Migração completa da UI, garantindo consistência visual e modernidade.</span>
                        </li>
                        <li class="flex gap-3">
                            <span class="text-emerald-500 mt-1">•</span>
                            <span><strong>Responsividade Total:</strong> Widgets, grids e tipografia ajustados para operar perfeitamente em Desktop, Tablet e Mobile.</span>
                        </li>
                        <li class="flex gap-3">
                            <span class="text-emerald-500 mt-1">•</span>
                            <span><strong>UX Refinada & Arquitetura:</strong> Uniformização de botões/dropdowns e refatoração de Controllers para espelhar a estrutura do Backend.</span>
                        </li>
                        <li class="flex gap-3">
                            <span class="text-emerald-500 mt-1">•</span>
                            <span><strong>Tratamento de Erros:</strong> Feedback visual aprimorado para falhas de conexão ou inconsistência de dados (Snackbars inteligentes).</span>
                        </li>
                    </ul>
                </div>
            </div>
        </section>

        <!-- Destaques Técnicos -->
        <section class="mb-16">
            <h2 class="text-2xl md:text-3xl font-bold text-white mb-6 border-b border-slate-800 pb-3 flex items-center gap-3">
                <span class="text-emerald-500">🛡️</span> Destaques Técnicos & Segurança
            </h2>
            
            <div class="space-y-6">
                <div>
                    <h3 class="text-xl font-semibold text-slate-100 mb-3">Backend (Python 3.13 + FastAPI)</h3>
                    <ul class="list-disc pl-6 space-y-2 text-slate-300 marker:text-slate-600">
                        <li><strong>Arquitetura Limpa:</strong> Separação estrita de responsabilidades (Services, Repositories, Controllers).</li>
                        <li><strong>Segurança OWASP:</strong> Autenticação JWT Stateless, Hashing com Bcrypt, Headers de segurança e validação com Pydantic v2.</li>
                        <li><strong>Performance & Types:</strong> Stack 100% assíncrona (ASGI) com SQLAlchemy 2.0 e cobertura de tipagem estática validada por Mypy.</li>
                    </ul>
                </div>
                
                <div>
                    <h3 class="text-xl font-semibold text-slate-100 mb-3">Frontend (Flutter 3.x)</h3>
                    <ul class="list-disc pl-6 space-y-2 text-slate-300 marker:text-slate-600">
                        <li><strong>Modularização:</strong> Organização por features (`features/`, `core/`, `shared/`) facilitando a escalabilidade.</li>
                        <li><strong>Gerenciamento de Estado & Ops:</strong> Uso de Provider (com transição para Riverpod), monitoramento de performance (`RouteTimingObserver`) e l10n pronto.</li>
                    </ul>
                </div>
            </div>
        </section>

        <!-- Roadmap -->
        <section class="mb-16">
            <h2 class="text-2xl md:text-3xl font-bold text-white mb-6 border-b border-slate-800 pb-3 flex items-center gap-3">
                <span class="text-emerald-500">🚀</span> Roadmap e Próximos Passos
            </h2>
            <p class="mb-6 text-slate-300">O desenvolvimento segue um ritmo acelerado focado na convergência entre <strong>Hardware (IoT)</strong> e <strong>Software</strong>.</p>

            <div class="grid md:grid-cols-2 gap-8">
                <div>
                    <h3 class="text-xl font-semibold text-emerald-400 mb-4 flex items-center gap-2">🚜 Automação e Agricultura</h3>
                    <ul class="space-y-3">
                        <li class="flex items-start gap-3 bg-slate-900/50 p-3 rounded-lg border border-slate-800">
                            <div class="w-5 h-5 rounded border-2 border-slate-600 mt-0.5 flex-shrink-0"></div>
                            <span class="text-slate-300"><strong class="text-white">Cálculo Hídrico de Precisão:</strong> Algoritmos baseados em evapotranspiração real e estágio da cultura.</span>
                        </li>
                        <li class="flex items-start gap-3 bg-slate-900/50 p-3 rounded-lg border border-slate-800">
                            <div class="w-5 h-5 rounded border-2 border-slate-600 mt-0.5 flex-shrink-0"></div>
                            <span class="text-slate-300"><strong class="text-white">IoT & Pivôs:</strong> Integração final para acionamento e telemetria remota de equipamentos de irrigação.</span>
                        </li>
                        <li class="flex items-start gap-3 bg-slate-900/50 p-3 rounded-lg border border-slate-800">
                            <div class="w-5 h-5 rounded border-2 border-slate-600 mt-0.5 flex-shrink-0"></div>
                            <span class="text-slate-300"><strong class="text-white">Validação de Campo:</strong> Testes de estresse das rotinas de automação em cenário real.</span>
                        </li>
                    </ul>
                </div>

                <div>
                    <h3 class="text-xl font-semibold text-emerald-400 mb-4 flex items-center gap-2">🔐 Sistema e Governança</h3>
                    <ul class="space-y-3">
                        <li class="flex items-start gap-3 bg-slate-900/50 p-3 rounded-lg border border-slate-800">
                            <div class="w-5 h-5 rounded border-2 border-slate-600 mt-0.5 flex-shrink-0"></div>
                            <span class="text-slate-300"><strong class="text-white">RBAC Completo:</strong> Finalização da interface para gestão visual de perfis e permissões de usuários.</span>
                        </li>
                        <li class="flex items-start gap-3 bg-slate-900/50 p-3 rounded-lg border border-slate-800">
                            <div class="w-5 h-5 rounded border-2 border-slate-600 mt-0.5 flex-shrink-0"></div>
                            <span class="text-slate-300"><strong class="text-white">Alertas Inteligentes:</strong> Automação de notificações baseadas em regras (ex: umidade < 20%).</span>
                        </li>
                        <li class="flex items-start gap-3 bg-slate-900/50 p-3 rounded-lg border border-slate-800">
                            <div class="w-5 h-5 rounded border-2 border-slate-600 mt-0.5 flex-shrink-0"></div>
                            <span class="text-slate-300"><strong class="text-white">RAG 2.0:</strong> Refinamento do modelo de IA para cruzar dados financeiros com dados agronômicos.</span>
                        </li>
                    </ul>
                </div>
            </div>
        </section>

        <!-- Stack Tecnológica -->
        <section class="mb-16">
            <h2 class="text-2xl md:text-3xl font-bold text-white mb-6 border-b border-slate-800 pb-3 flex items-center gap-3">
                <span class="text-emerald-500">🛠️</span> Stack Tecnológica Completa
            </h2>
            
            <div class="overflow-x-auto bg-slate-900 rounded-xl border border-slate-800 shadow-lg">
                <table class="w-full text-left border-collapse min-w-max">
                    <thead>
                        <tr class="bg-slate-800/80 text-emerald-400 text-sm uppercase tracking-wider">
                            <th class="p-4 border-b border-slate-700 font-semibold">Categoria</th>
                            <th class="p-4 border-b border-slate-700 font-semibold">Tecnologias Principais</th>
                            <th class="p-4 border-b border-slate-700 font-semibold">Detalhes</th>
                        </tr>
                    </thead>
                    <tbody class="text-slate-300 divide-y divide-slate-800/50">
                        <tr class="hover:bg-slate-800/30 transition-colors">
                            <td class="p-4 font-medium text-white">Mobile & Web</td>
                            <td class="p-4 font-bold text-blue-400">Flutter 3.x</td>
                            <td class="p-4">Material 3, Provider, Dart 3, Intl</td>
                        </tr>
                        <tr class="hover:bg-slate-800/30 transition-colors">
                            <td class="p-4 font-medium text-white">Backend API</td>
                            <td class="p-4 font-bold text-yellow-500">Python 3.13</td>
                            <td class="p-4">FastAPI, Uvicorn, Pydantic v2, APScheduler</td>
                        </tr>
                        <tr class="hover:bg-slate-800/30 transition-colors">
                            <td class="p-4 font-medium text-white">Banco de Dados</td>
                            <td class="p-4 font-bold text-blue-500">PostgreSQL 15+</td>
                            <td class="p-4">GeoAlchemy2 (Dados Espaciais), Alembic (Migrações)</td>
                        </tr>
                        <tr class="hover:bg-slate-800/30 transition-colors">
                            <td class="p-4 font-medium text-white">IA & LLM</td>
                            <td class="p-4 font-bold text-gray-300">Ollama / RAG</td>
                            <td class="p-4">Llama 3, Mistral, LangChain, Vector Search</td>
                        </tr>
                        <tr class="hover:bg-slate-800/30 transition-colors">
                            <td class="p-4 font-medium text-white">Infra & DevOps</td>
                            <td class="p-4 font-bold text-cyan-500">Docker</td>
                            <td class="p-4">GitHub Actions, Pytest, Flutter Test, Black/Isort</td>
                        </tr>
                    </tbody>
                </table>
            </div>
        </section>

        <!-- Rodapé -->
        <footer class="border-t border-slate-800 pt-10 text-center space-y-8">
            <div class="max-w-2xl mx-auto bg-slate-900/50 p-6 rounded-xl border border-slate-800">
                <h4 class="text-white font-bold mb-2 flex justify-center items-center gap-2">
                    <span class="text-emerald-500">🤝</span> Direitos Autorais
                </h4>
                <p class="text-sm text-slate-400 leading-relaxed">
                    Este é um software <strong>proprietário</strong>. O código-fonte e a propriedade intelectual pertencem exclusivamente ao seu autor. Este repositório público destina-se apenas à demonstração de capacidades técnicas de engenharia de software e portfólio.
                </p>
            </div>

            <div>
                <h3 class="text-2xl font-bold text-white mb-2">👨‍💻 Autor & Contato</h3>
                <p class="text-emerald-400 font-semibold text-lg mb-1">Robert Ferreira</p>
                <p class="text-slate-400 text-sm mb-6">Engenheiro de Software Full-Stack | Especialista em AgTech & IA</p>
                
                <div class="flex justify-center gap-4 mb-10">
                    <a href="https://www.linkedin.com/in/robert-guilherme-ferreira/" target="_blank" class="hover:scale-110 transition-transform opacity-90 hover:opacity-100">
                        <img src="https://img.shields.io/badge/-LinkedIn-0077B5?style=for-the-badge&logo=Linkedin&logoColor=white" alt="LinkedIn" class="h-8 rounded">
                    </a>
                    <a href="mailto:contato.robferreira@gmail.com" class="hover:scale-110 transition-transform opacity-90 hover:opacity-100">
                        <img src="https://img.shields.io/badge/-Gmail-D14836?style=for-the-badge&logo=Gmail&logoColor=white" alt="Gmail" class="h-8 rounded">
                    </a>
                    <a href="https://github.com/RobertGFerreira" target="_blank" class="hover:scale-110 transition-transform opacity-90 hover:opacity-100">
                        <img src="https://img.shields.io/badge/-Portfolio-181717?style=for-the-badge&logo=github&logoColor=white" alt="GitHub" class="h-8 rounded">
                    </a>
                </div>
                
                <p class="text-xs text-slate-500">&copy; 2025 Robert Ferreira. Todos os direitos reservados.</p>
                <p class="text-xs text-slate-500">Última atualização: 13 de março de 2026.</p>
            </div>
        </footer>

    </div>

</body>
</html>