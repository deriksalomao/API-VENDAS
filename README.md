API VENDAS
DOCUMENTAÇÃO
Iniciar o Serviço
Essas instruções ajudarão você a executar uma cópia do projeto em sua máquina local para desenvolvimento e testes. Para informações sobre como implantar o projeto em um sistema ativo, consulte a seção de implantação.

Design de Software
SOLID
Framework
SPRING FRAMEWORK
ORM
HIBERNATE
Funcionalidades para o usuário
Criar Usuário
Método: POST
URL: /usuario
Campos:
name
email
password
is_active
cpf_cnpj
Exemplo de curl:

curl -X POST http://localhost:8080/usuario \
     -H "Content-Type: application/json" \
     -d '{
           "name": "John Doe",
           "email": "john.doe@example.com",
           "password": "password123",
           "is_active": true,
           "cpf_cnpj": "12345678901"
         }'
Atualizar Usuário
Método: PUT
URL: /usuario/{id}
Campos:
name
email
password
is_active
cpf_cnpj
Exemplo de curl:

curl -X PUT http://localhost:8080/usuario \
     -H "Content-Type: application/json" \
     -d '{
           "name": "John Doe",
           "email": "john.doe@example.com",
           "password": "password123",
           "is_active": true,
           "cpf_cnpj": "12345678901"
         }'
Encontrar Usuário pelo ID
Método: GET
URL: /usuario
Exemplo de curl:

curl -X GET http://localhost:8080/usuario/{id}
Inativar ou Ativar usuário pelo ID
Método: PUT
URL: /usuario/{id}/status
Campos:
is_active
Exemplo de curl:

curl -X PUT http://localhost:8080/usuario/{id}/status \
     -H "Content-Type: application/json" \
     -d '{
           "is_active": false
         }'
