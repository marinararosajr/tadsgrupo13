# 🎬 Cinem@Fã - Quizzes interativos sobre filmes e séries - PoC

O *Cinem@Fã* é uma aplicação web interativa de perguntas e respostas focada no entretenimento de fãs de séries, cinema e televisão. O sistema permite aos utilizadores testarem os seus conhecimentos em diversas franquias famosas, acumularem pontos e competirem num ranking geral.

A finalidade desta PoC é comprovar a viabilidade técnica da plataforma interativa de quizzes. O foco é testar as etapas que o usuário vai percorrer durante o uso da aplicação: autenticação, escolha de tema e interação de perguntas e respostas, cálculo de pontuação e atualização em tempo real do ranking geral de pontos dos usuários.

Este projeto foi desenvolvido como requisito acadêmico pela *Equipe 13* do curso de *Análise e Desenvolvimento de Sistemas* do *Centro Universitário SENAC*.

---

## ▷ Instruções para execução

Para rodar os arquivos localmente na sua máquina, o projeto não exige instalações complexas. Apenas execute esses passos:

1. Faça o download deste repositório clicando no botão verde `<> Code`, e depois clique em "Download ZIP" no topo da página;
2. Extraia o ficheiro ZIP no seu computador;
3. Abra a pasta extraída e dê um duplo clique no arquivo index.html;
4. A aplicação abrirá diretamente no seu navegador padrão.

---

## 🚀 Resumo das funcionalidades da Cinem@Fã

*   Autenticação de utilizadores: Sistema de registo e login utilizando e-mail e senha.
*   Persistência de dados local: Utilização da API localStorage do navegador para guardar perfis de utilizadores, histórico de quizzes concluídos e pontuações, sem necessidade de uma base de dados externa.
*   Dinâmica de quizzes: 
    1.   Seis categorias de entretenimento disponíveis;
    2.   Sorteio dinâmico de dez perguntas aleatórias a partir de um banco de trinta questões por tema, garantindo que cada jogada seja única;
    3.   Bloqueio de repetição: cada utilizador só pode responder a cada tema uma única vez.
*   Feedback visual e imediato: Barra de progresso interativa, validação de respostas em tempo real e transições suaves de interface.
*   Gamificação: Tabela de classificação com ranking do top 5 atualizada automaticamente com base na pontuação total dos usuários.
*   Conformidade legal: Aviso de conformidade com a LGPD - Lei Geral de Proteção de Dados - Lei 13.709/18.

---

## 📚 Temas de quizzes disponíveis

1.  🌊 Percy Jackson
2.  🟢 Chaves
3.  🎠 Carrossel
4.  🪄 Harry Potter
5.  ⚔️ Demon Slayer
6.  🩺 Grey's Anatomy

---

## 💻 Tecnologias e padrões utilizados

O projeto foi construído utilizando as bases do desenvolvimento Web Standards, com as seguintes tecnologias:

*   HTML5 - Semântica e estruturação lógica de componentes.
*   CSS3 - Estilização responsiva (mobile-first), utilização de CSS Variables (:root), Flexbox e CSS Grid Layout.
*   JavaScript (Vanilla JS) - Manipulação de DOM, gestão de estado da aplicação, arrays/objetos, e persistência com localStorage.
*   Design - Interface baseada em "Cards" (modo escuro/dark theme) e tipografia moderna (Google Fonts: Poppins).

---

## ⚙️ Estruturação e funcionamento da PoC

Para viabilizar a construção rápida do protótipo funcional com foco na experiência do usuário, o sistema foi estruturado com arquitetura Client-Side (front-end) e persistência local, da seguinte forma:

*   Estrutura do front-end (interface e lógica): Estruturação semântica das telas e acessibilidade, estilização, identidade visual e design responsivo (Mobile-First), manipulação do DOM, controle de fluxo do quiz, validação de respostas, pontuação e integração com o armazenamento local;
*   Persistência de dados (simulação de banco de dados): JSON e localStorage, utilizados para armazenar a base de perguntas, respostas, histórico de pontuações e preferências do usuário diretamente no navegador;
*   Estrutura do back-end: Não aplicável na PoC. Toda a regra de negócio é executada no lado do cliente, eliminando a dependência de servidor para validação inicial da jornada, já que se trata apenas de um protótipo.


Considerando o desenvolvimento de um protótipo, o funcionamento da aplicação neste momento foi arquitetado para proporcionar:

*   Validação rápida: Uso de localStorage e arquivos JSON que simulam o comportamento de um banco de dados sem travar o desenvolvimento com configurações complexas de back-end neste momento, permitindo colocar o protótipo funcional nas mãos dos usuários rapidamente.   
*   Coleta de feedbacks reais: Como o sistema já roda de forma tangível no navegador, é possível testar a usabilidade, o layout responsivo e a lógica do quiz para coletar métricas e feedbacks reais antes de escalar o banco de dados.
*   Banco de dados simulado/armazenamento local: O localStorage junto com a estrutura JSON não é um Sistema Gerenciador de Banco de Dados (SGBD)  tradicional como MySQL ou PostgreSQL, mas nesse projeto ele funciona como uma camada de persistência de dados no navegador.

---

## 🛠️ Estrutura do projeto

```text
📦 cinemafa
 ┣ 📂 css
 ┃ ┗ 📜 style.css       # Estilos globais e responsividade da aplicação
 ┣ 📂 js
 ┃ ┣ 📜 app.js          # Lógica principal, manipulação de DOM e rotas virtuais
 ┃ ┗ 📜 data.js         # Banco de dados estático (perguntas, alternativas e respostas)
 ┣ 📜 index.html        # Estrutura principal da página (Single Page Application)
 ┣ 📜 db.json           # Representação JSON da estrutura de dados da aplicação
 ┗ 📜 README.md         # Documentação do projeto
 ```

---

## 📊 Resultados obtidos

A plataforma apresentou navegação fluida e aparência minimalista e limpa. Para uma futura evolução arquitetural, foi idealizado que o sistema estará preparado para integrar:
1. API RESTful desenvolvida em Node.js para o back-end;
2. Um banco de dados relacional, com migração da persistência local para SQLite ou SGBD equivalente, permitindo ranking global, autenticação de usuários e painel administrativo dinâmico.

---

## 👤 Integrantes do grupo responsáveis pelo projeto

 Desenvolvido por:
* Cristiane Ferreira (FênixxTec);
* Danielly Gomes de Souza (
daniellygdesouza-cyber);
* Helvia Monteiro Olmeda (HelviaMonteiro);
* Marinara de Jesus Rosa (marinararosajr);
* Polyanna Michele do Nascimento (polymichele);
* Rodrigo Martins de Almeida (xNumber01).
