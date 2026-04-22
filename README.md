Firebase Controle de Acesso

Esse projeto é uma aplicação web conectada ao Firebase com dois tipos de usuário: admin e user.

---

Como funciona

A aplicação usa Firebase Authentication para login e cadastro de usuários.

Quando a conta é criada, é salvo um cargo (role) no banco de dados.

Os cargos são:
- admin: tem acesso total
- user: tem acesso limitado

---

Estrutura do banco de dados

O banco foi organizado assim:

{
  "users": {
    "uid": {
      "email": "usuario@email.com",
      "role": "user"
    }
  },
  "admin-data": {
    "msg": "dados apenas do admin"
  }
}

---

Segurança

As regras do Firebase foram usadas para controlar o acesso.

O usuário comum só acessa dados básicos.

O admin acessa tudo, incluindo dados restritos.

---

O que a aplicação faz

- Cria e faz login de usuários
- Salva o tipo de usuário no banco
- Mostra conteúdos diferentes na tela dependendo do cargo
- Protege dados usando regras do Firebase

---

Tecnologias usadas

- HTML e JavaScript ou React
- Firebase Authentication
- Firebase Realtime Database

---

Resumo

Esse projeto mostra como separar usuários em admin e user usando Firebase, controlando o acesso aos dados e protegendo o banco com regras de segurança.
