💰 Moedas Escolares – Sistema de Moeda Estudantil

O Sistema de Moeda Estudantil – Moedas Escolares foi criado para valorizar o desempenho dos estudantes, tornando o reconhecimento do mérito algo visível, moderno e recompensador.

Professores distribuem moedas virtuais como incentivo, e alunos podem trocá-las por benefícios oferecidos pelas empresas parceiras.

O sistema promove:

🎯 Motivação dos alunos por recompensas reais

🔍 Transparência no acompanhamento de méritos

🤝 Conexão inovadora entre escolas, professores, empresas e estudantes

📊 Organização e automação de processos educacionais

🚀 Funcionalidades Principais
👨‍🎓 Cadastro de Alunos

Alunos registram nome, CPF, email e curso para participarem do programa.

👩‍🏫 Cadastro de Professores

Professores são responsáveis por distribuir moedas e acompanhar histórico dos alunos.

🏢 Cadastro de Empresas Parceiras

Empresas podem criar benefícios como produtos, serviços e descontos.

💸 Distribuição de Moedas

Professores recebem moedas periódicas que podem distribuir conforme o desempenho dos alunos.

✉️ Notificações Automáticas por E-mail

Via EmailJS, o sistema envia notificações de:

Recebimento de moedas

Resgate de benefícios

Redefinição de senha

🎁 Resgate de Benefícios

Alunos podem trocar moedas acumuladas por vantagens e recebem um código de resgate via e-mail.

🔐 Autenticação e Perfis

Perfis disponíveis:

Aluno

Professor

Empresa Parceira

Com suporte a:

Recuperação de senha via e-mail

Geração automática de nova senha

Validação segura com Spring Security

🛠️ Tecnologias Utilizadas
Backend – Spring Boot

☕ Java 17+

🟦 Spring Boot 3.3.4

🔐 Spring Security

🗄️ Spring Data JPA

🐘 PostgreSQL

📧 EmailJS + JavaMailSender

⚙️ Maven

Frontend – HTML/CSS/JS

🌐 HTML5

🎨 CSS3 (Glassmorphism Azul-Turquesa)

⚡ JavaScript

🔌 Consumo de API via Fetch

🏛️ Arquitetura do Sistema

O projeto segue boas práticas de arquitetura em camadas:

Controller → Service → Repository → Domain(Model)

Camadas

Controller – Endpoints REST para login, cadastro, moedas, benefícios etc.

Service – Regras de negócio (envio de email, reset de senha, distribuição de moedas).

Repository – Persistência via Spring Data JPA.

Domain/Model – Entidades do sistema, como:

Aluno

Professor

Empresa

Benefício

Menu

Evento

Ledger

⚙️ Instalação e Execução
✔️ Pré-requisitos

Java 17+

Maven 3.8+

PostgreSQL 12+

Navegador moderno

📥 Instalar Dependências

Clone o repositório:

git clone https://github.com/keijizn/Moedas-Escolares.git
cd Moedas-Escolares

▶️ Executar o Backend (Spring Boot)
cd backend
mvn spring-boot:run


A API estará disponível em:

👉 http://localhost:8080

📁 Estrutura de Pastas do Projeto
Moedas-Escolares/
│
├── backend/
│   ├── src/main/java/com/example/moeda/moedaestudantil/
│   │   ├── api/                # Controllers
│   │   ├── service/            # Regras de negócio
│   │   ├── repo/               # Repositórios JPA
│   │   ├── domain/             # Entidades
│   │   ├── security/           # Autenticação
│   │   └── dto/                # Objetos de transferência
│   ├── src/main/resources/
│   │   └── application.properties
│   └── pom.xml
│
├── frontend/
│   ├── assets/
│   ├── css/
│   ├── js/
│   └── *.html
│
└── README.md
