# Servidor construído usando Express, TypeORM, JSON Web Token, Bcrypt e PostgreSQL
Projeto usado para testar o acesso ao SGBD com TypeORM e o controle de acesso com JWT .

## Modelo de dados da aplicação

![Texto alternativo para a imagem](https://github.com/arleysouza/servidor-gasto-typeorm-jwt-bcrypt/blob/master/imagens/modelo.png)

É necessário setar os parâmetros de acesso ao SGBD PostgreSQL no arquivo `src/add-data-source.ts`.

## Observações
- Os parâmetros de conexão com o SGBD estão no arquivo `src/app-data-source.ts`;
- As entidades estão na pasta `src/entity`. As entidades `usuario` e `gasto` serão persistidas como tabelas do SGBD. Existe um relacionamento 1:n, um usuário pode ter vários gastos;
- A hierarquia de rotas está definida na pasta `src/routes`;
- A inicialização do servidor está no arquivo `src/index.ts` e para rodar a aplicação, em modo de desenvolvimento, usa-se o comando `npm run dev` e, em modo de produção, `npm run start`. Esses comandos foram definidos no arquivo de `package.json` da aplicação: 
```
"scripts": {
   "dev": "ts-node-dev src/index.ts",
   "start": "ts-node src/index.ts"
}
``` 