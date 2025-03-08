# NLW-Connect

Sistema de Indicações - Backend
Este é o backend de um sistema de indicações que organiza um ranking com base na quantidade de indicações realizadas por cada usuário. O projeto utiliza diversas tecnologias modernas para garantir escalabilidade, desempenho e manutenibilidade.

🚀 Tecnologias Utilizadas
Node.js: Plataforma para execução de JavaScript no backend.

Biome: Ferramenta para formatação e linting do código.

Docker: Contêineres para garantir consistência entre ambientes de desenvolvimento e produção.

PostgreSQL: Banco de dados relacional para armazenar as informações dos usuários e das indicações.

Redis: Sistema de cache para otimizar consultas frequentes e melhorar o desempenho.

Drizzle: ORM para manipulação e abstração das interações com o banco de dados.

📋 Pré-requisitos
Certifique-se de ter as seguintes ferramentas instaladas na sua máquina:

Node.js

Docker

Docker Compose

Além disso, é recomendado o uso de um bom editor de código, como o Visual Studio Code.

📦 Como Executar
Clone o Repositório

bash
git clone https://github.com/seu-usuario/sistema-indicacoes-backend.git

cd sistema-indicacoes-backend

Configure as Variáveis de Ambiente

Crie um arquivo .env na raiz do projeto com as seguintes variáveis:

DATABASE_URL=postgresql://docker:docker@localhost:5432/connect
REDIS_URL=redis://localhost:6379
PORT=3333
Inicie o Docker Certifique-se de que o Docker está em execução e execute o seguinte comando para subir os contêineres:

bash
docker-compose up --build
Execute as Migrações do Banco Após os contêineres estarem ativos, aplique as migrações do banco de dados usando o Drizzle:

bash
npm run migrate
Inicie a Aplicação Agora, inicie o servidor:

bash
npm run start
Acesse o Sistema A aplicação estará acessível em http://localhost:3333.

🛠️ Estrutura do Projeto
📂 src

 ┣ 📂 controllers
 
 ┣ 📂 models
 
 ┣ 📂 routes
 
 ┣ 📂 services
 
 ┣ 📂 utils
 
 ┗ index.js
 
controllers: Controladores responsáveis por lidar com as requisições.

models: Definições de entidades e esquemas do banco de dados.

routes: Configuração das rotas da aplicação.

services: Lógica de negócios.

utils: Funções utilitárias.

🏆 Funcionalidades
Registro de indicações realizadas por usuários.

Organização de um ranking em tempo real.

Cache para otimização de desempenho.

API RESTful para integração com o frontend.

🧪 Testes
Execute os testes automatizados para garantir a estabilidade do sistema:

bash
npm run test

🛡️ Segurança
Use variáveis de ambiente para armazenar informações sensíveis.

Configure permissões adequadas nos contêineres e serviços externos.

📝 Licença
Este projeto está sob a licença MIT. Consulte o arquivo LICENSE para mais informações.
