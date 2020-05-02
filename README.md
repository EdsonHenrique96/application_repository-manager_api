# Repository Manager

Uma API REST, que tem como finalidade o gerenciamento de repositórios do github.
Com ela você pode Criar, Editar, listar, Deletar e dar likes nos seus repositórios.

Nota: Não há persistência de dados e todos seus dados ficam em memória.

## Como usar

1. Clone o repositório para o seu ambiente
```bash
git clone ${repositoryDownloadURL}
```

2. Instale as depedências
```bash
cd repository-manager
yarn install
```

3. Inicie a aplicação (API)
```bash
yarn dev
```
Obs: Por padrão a aplicação ficará disponível na port 3333 do seu localhost. Acesse http://localhost:3333

## Rotas

Você vai precisar de um cliente HTTP para conseguir acessar a maioria das rodas exeto a roda GET que é possivel acessa-la através do browser.

Cliente HTTP sugerido : [Insomnia](https://insomnia.rest)

Criar um repositório
```json
POST /repositories

Request body
{
 "title": "Repositório de exemplo",
 "url": "https://github.com/EdsonHenrique96",
 "techs": ["Nodejs", "React", "React Native"]
}

```
Listar todos os repositórios
```
GET /repositories
```

Listar repositórios por id ou por nome (TODO)

Editar repositório
```json
PUT /repositories/:id

Request body
{
 "title": "Repositório de exemplo atualizado",
 "url": "https://github.com/EdsonHenrique96",
 "techs": ["Typescript", "Vuejs", "Flutter"]
}
```

Deletar repositório
```
DELETE /repositories/:id
```

Dar like em um repositório
```
POST /repositories/:id/like

No request body
```

Se você usa curl, temos algumas requisões prontas [curl - Request exemples](https://github.com/EdsonHenrique96/repository-manager/blob/master/auxiliary-tools/curl/request-exemples.md)
## Testes

Para rodar os teste funcionais
```bash
yarn test
```

## Tecnologias e bibliotecas

- Nodejs (plataforma que permite usar javascript no servidor)
- Express (Framework http)
- uuid (Biblioteca para manipulação de uuid)
- jest (Biblioteca de testes)



