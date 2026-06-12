# 📚 Sistema de Análises Críticas para Incentivo à Leitura

## 📖 Sobre o Projeto
O Sistema de Análises Críticas para Incentivo à Leitura é uma plataforma web desenvolvida para mitigar o declínio do engajamento literário no ambiente educacional. O sistema funciona como um acervo gerenciado pelos docentes, onde os professores cadastram livros e artigos e os estudantes participam ativamente consumindo as obras, inserindo comentários e atribuindo avaliações críticas. Ao fomentar um ambiente digital interativo, a plataforma busca promover o pensamento crítico, a usabilidade e a troca de conhecimentos de forma colaborativa e dinâmica.

## 🎯 Objetivos

**Objetivo Geral**
Desenvolver um ambiente digital interativo voltado ao compartilhamento de comentários e avaliações de obras, visando incentivar o hábito da leitura e promover o pensamento crítico no meio educacional.

**Objetivos Específicos**
* Fornecer um repositório centralizado de obras literárias (livros e artigos) gerenciado por professores.
* Disponibilizar ferramentas estruturadas para que os alunos façam comentários e avaliações críticas nas obras.
* Estimular a interação social e o debate acadêmico dentro da comunidade escolar.
* Oferecer mecanismos de busca e filtros eficientes por categorias e gêneros.
* Prover ferramentas de moderação e análise de engajamento para os administradores.

## 👥 Público-Alvo
* **Estudantes:** Usuários que consomem o acervo literário, realizam buscas e publicam seus comentários e avaliações sobre as obras.
* **Professores / Administradores:** Responsáveis por alimentar o repositório cadastrando novos livros, gerenciar categorias, orientar as discussões e moderar os comentários.
* **Instituições de Ensino:** Escolas e faculdades que buscam integrar ferramentas tecnológicas para complementar práticas pedagógicas de leitura.

## ✨ Funcionalidades
* **Cadastro de usuários:** Registro seguro de alunos e professores com distinção de perfis.
* **Login e autenticação:** Acesso restrito via credenciais validadas com controle de sessão.
* **Perfil do usuário:** Personalização de dados e biografia do leitor.
* **Cadastro de conteúdos:** Inserção de obras no catálogo institucional (exclusivo para professores).
* **Comentários e avaliações:** Espaço para os alunos digitarem suas impressões críticas e atribuírem notas às obras.
* **Busca global e filtros:** Localização rápida de livros por categoria, autor ou palavra-chave.
* **Moderação de conteúdo:** Ferramentas administrativas para exclusão de interações indevidas.

## 📋 Requisitos Funcionais
* **RF01 - Gestão de Autenticação e Perfil:** O sistema deve permitir que o usuário crie uma conta, recupere senha e personalize seu perfil de leitor.
* **RF02 - Repositório de Obras:** Funcionalidade exclusiva do professor para cadastrar conteúdos (Título, Autor, Descrição, Imagem) que servirão de base para o sistema.
* **RF03 - Motor de Interação Social:** Espaço para o aluno digitar comentários e atribuir avaliações/notas associadas a um conteúdo específico.
* **RF04 - Busca e Filtros:** Mecanismo para localização rápida de conteúdos por meio de categorias ou palavras-chave.

## ⚙️ Requisitos Não Funcionais
* **RNF01 - Responsividade:** A interface deve adaptar-se automaticamente a diferentes tamanhos de tela (abordagem Mobile-First).
* **RNF02 - Disponibilidade:** O sistema deve estar acessível via web com alta disponibilidade sob uma arquitetura Cliente-Servidor.
* **RNF03 - Usabilidade:** O tempo de aprendizado para um novo usuário não deve ultrapassar 5 minutos devido à interface simplificada.
* **RNF04 - Performance:** O carregamento da página inicial não deve exceder 2 segundos em conexões padrão.
* **RNF05 - Integridade:** O banco de dados deve seguir o modelo relacional normalizado, garantindo consistência por meio de chaves estrangeiras.

## 🏗️ Arquitetura do Sistema
* **Arquitetura Cliente-Servidor:** O sistema separa as responsabilidades de visualização (cliente) das lixas de negócio e persistência (servidor).
* **Front-end:** Camada de apresentação processada via navegador, construída com foco em responsividade para coletar as interações dos alunos e exibir os dados do acervo.
* **Banco de Dados Relacional:** Armazenamento centralizado que garante suporte a transações estáveis, restrições de chaves e consultas otimizadas através de junções (`INNER JOIN`).

## 🗄️ Modelo de Dados
* **Usuários e Tipo de Usuário:** Armazena as credenciais e define o nível de acesso (Aluno ou Professor).
* **Conteúdo e Categoria:** Representa as obras literárias cadastradas pelos professores, devidamente organizadas por suas respectivas categorias.
* **Comentário:** O elo de interação do sistema, onde o aluno vincula seu comentário e sua nota a um conteúdo específico do acervo.

## 💻 Tecnologias Utilizadas

| Tecnologia | Finalidade |
| :--- | :--- |
| **HTML5** | Estrutura semântica das páginas web |
| **CSS3** | Estilização responsiva e design visual |
| **JavaScript** | Manipulação do DOM, lógicas algorítmicas e interatividade |
| **PostgreSQL / MySQL** | Banco de Dados Relacional e persistência de dados |
| **Git** | Controle de versão de código local |
| **GitHub** | Repositório em nuvem, gerenciamento ágil (Kanban) e Pull Requests |
| **VS Code** | Ambiente de Desenvolvimento Integrado (IDE) |
| **Figma** | Prototipação das interfaces e design UI/UX |
| **brModelo** | Modelagem conceitual e lógica do banco de dados |
| **Lucidchart** | Criação de diagramas UML e Engenharia de Software |
| **MySQL Workbench** | Modelagem física e administração do banco de dados |
| **Cisco Packet Tracer** | Simulação da arquitetura de conectividade e infraestrutura da rede |
| **Canva** | Design do banner acadêmico e identidade visual |
| **Stitch** | Componentização e documentação visual do projeto |

## 🔄 Fluxo de Utilização
1. **Cadastro e Login:** O usuário realiza seu registro e acessa a plataforma com sua respectiva permissão (Aluno ou Professor).
2. **Alimentação (Professor):** O professor cadastra os livros e artigos vinculando-os a uma categoria.
3. **Consulta (Aluno):** O aluno navega pelo Dashboard, utiliza a busca global e seleciona uma obra do catálogo.
4. **Interação (Aluno):** O aluno digita seu comentário, atribui sua avaliação e o sistema associa essa interação ao perfil dele e ao livro selecionado.

## 🌐 Infraestrutura
* **Rede LAN:** Configuração física em estrela baseada no ambiente de laboratório institucional.
* **Access Point:** Emissão de sinal Wi-Fi para permitir o acesso responsivo via dispositivos móveis.
* **Servidores Dedicados:** Divisão estrutural simulada contendo Servidor Web, Servidor de Banco de Dados e Servidor DNS para resolução de nomes locais.

## 📱 Interface
* **Dashboard:** Painel dinâmico que exibe os carrosséis de livros e o resumo do acervo.
* **Sidebar e Navbar:** Menus fixos estruturados com ícones limpos para guiar a navegação do usuário.
* **Área de Destaques e Busca Global:** Seções focadas em sugerir leituras ("Top 10") e permitir buscas instantâneas no topo da tela.

## 🚀 Possíveis Melhorias Futuras
* Sistema de recomendações com IA baseado no histórico de leituras do aluno.
* Gamificação completa com ranking de leitores e conquistas por objetivos alcançados.
* Aplicativo mobile nativo para iOS e Android.
* Integração via API com bibliotecas digitais externas.

## 👨‍💻 Equipe
* Lívia Ghirardi do Amaral
* Rafaela da Paz
* Tuanny Tomazelli

## 📚 Contexto Acadêmico
Projeto Integrador desenvolvido para o curso superior de Tecnologia em Análise e Desenvolvimento de Sistemas da Escola e Faculdade de Tecnologia SENAI Gaspar Ricardo Junior (Sorocaba/SP).

## 📄 Licença
Distribuído sob a licença MIT.
