# Projeto Módulo 3 – Low Code / No Code / Vibecode

**Disciplina:** Engenharia de Prompt e Aplicações em IA  
**Professor(a):** Kadidja Valéria  
**Data:** 05/11/2026  
**Turma:** ENG. SOFT + SI – 6ª feira – SEDE UDF  
**Alunos:**Guilherme Behrmann e Guilherme silva

---

## 📌 Desafio Escolhido

A equipe desenvolveu  o **HealthSchedule**, um aplicativo web de bares em brasilias ,focado em da ao usuario a opção de escolher algo de qualidade ou do seu estilo musical

**Problema resolvido:** Facilitar a buscar e filtrar suas opcoes determinando o tipo , o estilo ,a faixa de preço e por fim a qualidade do bar 
**Funcionalidades desenvolvidas:**
- 🔍 Dicas de saude ,deixando claro que apesar de beber ser uma diversão deve ser feita com responsabilidade
- 🗺️ Regioes de brasilia ,para filtrar sua busca
- 🚨 Agendar visita e copiar convite(informando ao proprietario a sua visita e quantas pessoas são alem de copiar convite para enviar para seus amigos e marcar o evento)
- 📋 Filtro (qualidade em estrelas de 1-5,estilo musical,faixa de preço e eventos de show ao vivo)
- 🌙- Resumo  e descrição completa de cada bar em funcionalidade no aplicativo


---

## 🖥️ Protótipo

**Acesso ao projeto**  
O protótipo completo está disponível no arquivo `index.html` — basta abrir no navegador.

**Estampas das telas**  
Consulte a pasta `/docs` para visualizar as impressões de cada tela.

| Tela | Descrição |
| :--- | :--- |
| `tela-home.png` | Página principal  |
| `tela-de-regioes-eventos-marcados.png` | Filtro de regiao e evento ja marcado |
| `tela-filtro.png` | filtro de qualidade,tipo,local e preço|
| `tela-de-agendamento.png` | Agendar evento |
| `tela-opção-bares.png` |bares e suas descrições|

**Como o app funciona:**
1. Abra o site `https://magical-crumble-82e185.netlify.app/` no navegador.
2. visulize as opçoes ou busque pela area ou bar que deseja .
3. Clique em qualquer cartão de bar ver descrição completa .
4. Use o botão "agendar" para marca o seu evento .
5. Experimente o botão copiar convite para whatsapp para enviar um convite detalhado do evento.
---

## ⚙️ Plataforma Utilizada no HealthSchedule

**Bubble.io — Desenvolvimento No-Code / Low-Code**e ** Ai Studio**

**Justificativa da escolha:**  
A ferramenta foi escolhida por ser uma das plataformas No-Code mais robustas para a criação de aplicações web completas (Full-Stack). Para o escopo do **HealthSchedule**, o Bubble permitiu desenvolver a interface do guia de bares, modelar o banco de dados do catálogo e criar a lógica de agendamento de rolês em um único ambiente visual, acelerando o desenvolvimento sem a necessidade de codificação manual tradicional. o Google AI Studio se enquadra perfeitamente nesse conceito, mas atua dentro de um nicho muito específico: ele é uma ferramenta Low-Code/No-Code voltada para Inteligência Artificial Generativa.

**Características que motivaram a escolha:**
- Desenvolvimento visual interativo (Drag-and-Drop) com motor de responsividade para adaptar a interface tanto para o celular da galera no bar quanto para o desktop.
- Banco de dados em nuvem integrado nativamente, essencial para armazenar o catálogo de bares de Brasília e os agendamentos dos usuários.
- Criação de regras de negócio através de fluxos de trabalho visuais ("Workflows"), ideais para estruturar a verificação das metas de redução de danos.
- Deploy em um clique, com ambientes de teste e produção gerenciados pela própria plataforma.

---

## ✅ Vantagens Identificadas no Projeto

- **Velocidade de prototipação Full-Stack:** O HealthSchedule foi criado rapidamente de ponta a ponta. O Bubble permitiu criar o painel principal, os cards dos bares, os modais interativos e o registro real dos agendamentos no backend quase simultaneamente.
- **Banco de Dados Real e Estruturado:** Em vez de depender de dados estáticos, foi possível estruturar tabelas reais (*Data Types*) para os Bares, Eventos ao Vivo e Cronogramas de Saúde. Também utilizamos *Option Sets* para gerenciar as Regiões Administrativas do DF (Asa Sul, Águas Claras, Sudoeste, etc.).
- **Implementação facilitada de lógicas complexas:** Construir o sistema de busca do app (cruzando filtros de texto, faixa de preço, estilo musical e região geográfica) foi resolvido usando os operadores nativos de busca do Bubble (*Do a search for*). Além disso, a montagem dinâmica do texto de convite para o WhatsApp — incluindo as tags de metas de hidratação, teto de gastos e transporte seguro — foi facilmente orquestrada via Workflows.
- **Sincronização global de agendamentos:** O armazenamento em nuvem do Bubble permitiu que os dados de agendamentos e metas de saúde fossem salvos no banco de dados e atrelados a usuários reais, permitindo que as pessoas acessem seus cronogramas de qualquer dispositivo.

---

## ⚠️ Limitações Encontradas

- **Limitações na personalização visual fina:** Embora entregue um design moderno, replicar a identidade noturna e "neon" do HealthSchedule (como desfoques de fundo complexos, cards em gradiente, alertas piscantes e animações de entrada) é mais rígido no Bubble. Efeitos que seriam simples no Tailwind CSS exigem o uso de plugins extras ou injeção manual de código HTML/CSS na plataforma.
- **Curva de aprendizado do motor responsivo:** Ajustar os contêineres para que os `BarCards` ou o formulário de `SchedulerForm` não quebrassem em telas menores exigiu tempo para dominar o sistema de alinhamento flexível do Bubble.
- **Lock-in tecnológico (Dependência da Plataforma):** O projeto do HealthSchedule fica totalmente atrelado à infraestrutura da empresa. Não é possível exportar o código-fonte da aplicação para hospedar em outro servidor ou evoluir para frameworks tradicionais no futuro.
- **Gestão de Performance e Escala:** Caso o catálogo do HealthSchedule passe a cobrir todos os bares do Distrito Federal, ou caso muitos usuários comecem a realizar pesquisas cruzando vários filtros simultaneamente, a aplicação pode sofrer gargalos de carregamento nos planos iniciais do Bubble, exigindo otimizações severas na arquitetura das buscas.
## 📚 Reflexão Crítica

**Como lidamos com as limitações da plataforma:**
- **Performance em buscas complexas:** Como o aplicativo realiza cruzamento de múltiplos filtros (região geográfica, faixa de preço, estilo musical e eventos ao vivo), utilizamos *Option Sets* do Bubble para gerenciar dados imutáveis (como a lista de Regiões Administrativas do DF). Isso alivia as consultas ao banco de dados principal e garante que a interface de busca permaneça rápida.
- **Consistência visual do catálogo:** Para contornar a lentidão de carregamento de fotos pesadas ou o risco de links externos quebrados para imagens de fachada dos bares, projetamos um banco de dados focado em uma UI tipográfica e colorida. Utilizamos emojis representativos (ex: 🍻, 🍷, 🍔) atrelados a campos de gradiente de cor específicos para cada local, garantindo consistência visual e velocidade de renderização na vitrine.
- **Lock-in Tecnológico:** A dependência da infraestrutura do Bubble foi mitigada adotando a mentalidade de que esta versão do HealthSchedule atua como um **MVP (Produto Mínimo Viável)**. O objetivo principal é validar rapidamente a adesão dos usuários às dinâmicas de redução de danos na boemia de Brasília. Caso haja necessidade de escalar massivamente no futuro, os dados (Bares, Agendamentos, Metas) podem ser facilmente exportados via CSV/API para migração.

**Aprendizado sobre o ecossistema No-Code / Low-Code:**
- O sucesso no Bubble depende muito mais da arquitetura de dados prévia (modelagem relacional de tabelas) do que do simples ato de "arrastar e soltar" elementos na tela.
- É essencial dominar o uso do modo *Debug (Step-by-Step)* para revisar os Workflows gerados. Detalhes sutis da lógica de negócios — como garantir que o checkbox de hidratação ou o teto de gastos sejam registrados corretamente no agendamento — exigem atenção técnica rigorosa.
- O No-Code acelera o processo e democratiza a criação, mas exige que o criador aplique fundamentos sólidos de Engenharia de Software (UX/UI, escalabilidade de banco de dados, privacidade e segurança) para que o resultado final seja uma aplicação funcional e não apenas um desenho de tela.
---

## 👥 Colaboração

**Organização:** A dupla focou em utilizar a aula para realizar o inicio do projeto e em casa atravez de chamdas delimitamos o que fazer e concluimos o projeto
| Integrante | Responsabilidades |
| :--- | :--- |
| **Guilherme Silva** | **Desenvolvimento & Prompt Engenharia:** Elaboração de prompts, revisão de código,Pesquisa e documentação, analise critica.
| **Guilherme Behrmann | **Design e UX:** Definição visual, revisão de layout, testes de usabilidade, impressões do protótipo ,Pesquisa e Documentação:** Pesquisa de plataformas, redação do README, análise crítica, organização do repositório |

---

## 📝 Registro da Aula

| Campo | Informações |
| :--- | :--- |
| **Data** | 11/05/2026 |
| **Atividade** | Discussão crítica + miniprojeto de aplicação |
| **Local** | Laboratório de informática / Quadro branco |
| **Professor(a)** | Kadidja Valéria |
| **Disciplina** | Engenharia de Prompt e Aplicações em IA |

---

## 🚀 Próximos Passos

- [ ] Implementar login social (Google OAuth / Apple) para criação de perfis de usuários e salvamento definitivo do histórico de rolês em nuvem.
- [ ] Integrar APIs de localização (Google Maps) para calcular rotas e estimativas de preço de transporte (Uber/99) em tempo real, reforçando a meta de retorno seguro.
- [ ] Configurar notificações push para enviar lembretes ativos das metas de redução de danos (ex: "Hora de beber um copo d'água!") durante o período do evento agendado.
- [ ] Otimizar a interface responsiva e empacotar a aplicação Bubble como um PWA (Progressive Web App), garantindo uma experiência fluida no celular durante a noite.
- [ ] Criar um sistema de check-out "Pós-Rolê" gamificado, onde o usuário avalia o bar e registra se conseguiu cumprir o teto de gastos e as metas de hidratação.
- [ ] Desenvolver um painel administrativo para donos de bares da região de Brasília reivindicarem seus perfis, atualizarem o cardápio e gerenciarem a agenda de eventos ao vivo.
---
* UDF 2026.*
