# Apoio-a-Leitura
# 📚 Sistema de Análises Críticas para Incentivo à Leitura

## 📖 Sobre o Projeto
O Sistema de Análises Críticas para Incentivo à Leitura é uma plataforma web desenvolvida para mitigar o declínio do engajamento literário no ambiente educacional. O sistema permite que os estudantes publiquem, compartilhem e discutam análises críticas sobre livros e artigos. Ao fomentar um ambiente digital interativo, a plataforma busca reverter a baixa adesão à leitura, promovendo o pensamento crítico, a usabilidade e a troca de conhecimentos de forma colaborativa e dinâmica.

## 🎯 Objetivos

**Objetivo Geral**
Desenvolver um ambiente digital interativo voltado à criação e ao compartilhamento de análises críticas, visando incentivar o hábito da leitura e promover o pensamento crítico no meio educacional.

**Objetivos Específicos**
* Fornecer um repositório centralizado de obras literárias (livros e artigos).
* Disponibilizar ferramentas estruturadas para redação e publicação de resenhas críticas.
* Estimular a interação social por meio de comentários e validação mútua (curtidas).
* Oferecer mecanismos de busca e filtros eficientes para exploração do acervo.
* Prover relatórios de engajamento e ferramentas de moderação para administradores e docentes.

## 👥 Público-Alvo
* **Estudantes:** Usuários centrais que consumirão o acervo literário, vizualizarão as resenhas e interagirão com seus pares no sistema.
* **Professores:** Usuários com perfil administrativo/orientador, responsáveis por cadastrar acervos, orientar discussões, moderar conteúdos e analisar o progresso de leitura.
* **Instituições de ensino:** Escolas e faculdades que buscam integrar ferramentas tecnológicas para complementar práticas pedagógicas e métricas de leitura extracurricular.

## ✨ Funcionalidades
* **Cadastro de usuários:** Registro seguro de alunos e professores na plataforma.
* **Login e autenticação:** Acesso via credenciais criptografadas com controle e validação de sessão.
* **Perfil do usuário:** Personalização de biografia literária e gestão de dados pessoais.
* **Cadastro de livros:** Inserção de obras no catálogo institucional (título, autor, editora, gênero, sinopse).
* **Publicação de resenhas:** Editor integrado para redação da análise crítica com atribuição de nota (1 a 5).
* **Comentários:** Espaço dedicado para interações e discussões em resenhas específicas.
* **Curtidas/interações:** Validação social das análises publicadas por outros usuários.
* **Busca de livros:** Ferramenta global de localização rápida no acervo literário.
* **Filtros:** Opções de refinamento da pesquisa por categoria, autor, gênero ou palavra-chave.
* **Relatórios administrativos:** Extração de métricas de engajamento estudantil e volume de leitura.
* **Moderação de conteúdo:** Ferramentas para exclusão de publicações indevidas, gestão de denúncias e manutenção das diretrizes da comunidade.

## 📋 Requisitos Funcionais
* **RF01 - Gestão de Perfil:** O sistema deve permitir que o usuário crie uma conta, recupere senha e personalize seu perfil de leitor.
* **RF02 - Repositório de Obras:** Funcionalidade para cadastrar livros (Título, Autor, Gênero) que servirão de base para as análises.
* **RF03 - Editor de Análises:** Espaço para redação de textos críticos com suporte a formatação básica e vinculação obrigatória a um livro e a uma nota.
* **RF04 - Motor de Interação:** Sistema de comentários em tempo real e botão de "curtir" para validação social das resenhas.
* **RF05 - Filtros de Busca:** Localização rápida de análises por categoria, autor ou palavra-chave.

## ⚙️ Requisitos Não Funcionais
* **RNF01 - Responsividade:** A interface deve adaptar-se automaticamente a diferentes tamanhos de tela (abordagem Mobile-First).
* **RNF02 - Disponibilidade:** O sistema deve estar acessível via web com alta disponibilidade sob uma arquitetura Cliente-Servidor.
* **RNF03 - Usabilidade:** O tempo de aprendizado para um novo usuário realizar sua primeira interação não deve ultrapassar 5 minutos.
* **RNF04 - Performance:** O carregamento da página inicial não deve exceder 2 segundos em conexões padrão.
* **RNF05 - Integridade:** O banco de dados deve seguir o modelo relacional normalizado (até a 3FN) garantindo integridade referencial.

## 🏗️ Arquitetura do Sistema
* **Arquitetura Cliente-Servidor:** O sistema baseia-se num fluxo bidirecional de comunicação, separando as responsabilidades de visualização (cliente) das lógicas de negócio e persistência (servidor).
* **Front-end:** A camada de apresentação (cliente) é processada via navegador, construída para ser responsiva e interativa, encarregada de recolher os dados dos usuários e exibir as informações de retorno em tempo real.
* **Banco de Dados Relacional:** O armazenamento é centralizado através do SGBD PostgreSQL, que garante o suporte a transações ACID, restrições e exclusão em cascata (Cascade Delete) garantindo que não existam registros órfãos.
* **Fluxo geral da aplicação:** O usuário interage com as interfaces web gerando requisições HTTP; o servidor valida regras de negócio (como login e notas válidas entre 1 e 5), comunica-se com o banco relacional para leitura ou escrita (CRUD) e devolve a resposta atualizada para compor dinamicamente a tela do usuário.

## 🗄️ Modelo de Dados
* **Usuário:** Tabela responsável por guardar as credenciais de acesso, biografia e histórico. Relaciona-se num escopo (1:N) tanto com Resenhas quanto com Comentários.
* **Livro:** Entidade base do acervo oficial. Contém atributos como título, autor, gênero e capa. Relaciona-se (1:N) com a entidade Resenha.
* **Resenha:** O núcleo do sistema. Atua como um elo dependente que exige a ligação via chaves estrangeiras (FK) de um Livro validado e de um Usuário autenticado.
* **Comentário:** Dependência social direta, obrigatoriamente referenciando uma Resenha pré-existente e um Usuário emissor.

## 💻 Tecnologias Utilizadas

| Tecnologia | Finalidade |
| :--- | :--- |
| **HTML5** | Estrutura semântica das páginas web |
| **CSS3** | Estilização responsiva (Grid/Flexbox) e design visual |
| **JavaScript** | Manipulação do DOM, lógicas algorítmicas e interatividade |
| **PostgreSQL** | Banco de Dados Relacional, persistência e integridade referencial |
| **Git** | Controle de Versão de código e ramificações (Branches) |
| **GitHub** | Repositório em nuvem, controle de projetos (Kanban) e Pull Requests |
| **Cisco Packet Tracer** | Simulação da arquitetura de conectividade e infraestrutura da rede |

## 🔄 Fluxo de Utilização
1. **Cadastro:** O estudante ou professor preenche os dados cadastrais básicos inserindo um registro na plataforma.
2. **Login:** As credenciais são inseridas, validadas, e a sessão é liberada permitindo o acesso a recursos de interação.
3. **Consulta de livros:** O usuário explora o catálogo da instituição listado na página principal.
4. **Escrita de resenhas:** O usuário seleciona uma obra, atribui uma avaliação e formaliza seu pensamento crítico via editor integrado.
5. **Comentários:** Outros membros da comunidade visualizam a resenha recém-publicada e deixam suas opiniões.
6. **Interação com a comunidade:** Geração de curtidas, réplicas e discussão fomentando um ambiente de validação acadêmica contínua.

## 🌐 Infraestrutura
O ambiente que sustenta a aplicação segue diretrizes robustas de redes simuladas:
* **Rede Cliente-Servidor:** Os dispositivos do laboratório atuam unicamente solicitando dados enquanto máquinas dedicadas provêm os serviços.
* **Servidor Web:** Ponto de hospedagem que responde às chamadas HTTP/HTTPS para servir as páginas do sistema.
* **Servidor Banco de Dados:** Isolado para processar exclusivamente a gestão do SGBD e garantir segurança física das informações.
* **Servidor DNS:** Atribui e resolve nomes de domínio locais para IPs, facilitando a memorização do acesso à rede pelos alunos.
* **Rede LAN:** Configuração física em estrela do laboratório escolar.
* **Access Point:** Ponto de emissão Wi-Fi permitindo a entrada dos smartphones (abordagem Mobile-First) na rede local de forma segura.
* **Segmentação de rede:** Utilização de Switches e Roteadores segmentando logicamente a rede de alunos do ambiente gerencial corporativo.

## 📱 Interface
O protótipo de alta fidelidade destaca abordagens de UX/UI como o "Dark Mode" e a fluidez do carregamento visual:
* **Dashboard:** Painel principal concentrando um resumo das atividades recentes da rede de leitura.
* **Sidebar:** Menu de navegação lateral fixa, reunindo ícones limpos para "Início", "Livros" e "Notificações".
* **Navbar:** Barra de navegação do topo com acesso ao perfil do usuário ativo e centralização visual rápida.
* **Área de Destaques:** *Hero Section* interativa exibindo os "Top 10 Livros" e o inteligente bloco de "Continuar lendo".
* **Busca Global:** Campo universal situado no topo para varredura dinâmica, não exigindo navegação extra para iniciar procura de obras ou autores.

## 🚀 Possíveis Melhorias Futuras
* Sistema de recomendações com IA (Machine Learning) baseado nos gêneros consumidos.
* Gamificação completa das etapas de desenvolvimento de leitura.
* Ranking de leitores contabilizando top resenhistas ou meta anual de leitura do aluno.
* Aplicativo mobile nativo para iOS e Android garantindo o suporte avançado de notificações.
* Integração com bibliotecas digitais externas via APIs de terceiros.
* Sistema de conquistas (*badges/insígnias digitais*) recompensando diferentes estágios da jornada literária.

## 👨‍💻 Equipe
* Lívia Ghirardi do Amaral
* Rafaela da Paz
* Tuanny Tomazelli

## 📚 Contexto Acadêmico
Projeto Integrador desenvolvido sob o formato interdisciplinar para o curso superior de Tecnologia em Análise e Desenvolvimento de Sistemas do SENAI (Escola e Faculdade de Tecnologia SENAI Gaspar Ricardo Junior - Sorocaba/SP).
