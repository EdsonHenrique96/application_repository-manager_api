## Requisições

GET /repositories
```bash
curl --request GET \
  --url http://localhost:3333/repositories
```

POST /repositories
```bash
curl --request POST \
  --url http://localhost:3333/repositories \
  --header 'content-type: application/json' \
  --data '{
	"title": "meu primeiro projeto",
	"url": "https://github.com/EdsonHenrique96",
	"techs": ["reactjs", "nodejs", "react native"]
}'
```

PUT /repositories/:id
```bash
curl --request PUT \
  --url http://localhost:3333/repositories/${repositoryId} \
  --header 'content-type: application/json' \
  --data '{
	"title": "Meu Projeto Top",
	"url": "https://github.com/EdsonHenrique96",
	"techs": ["angular", "php", "laravel"]
}'
```

DELETE /repositories/:id
```bash
curl --request DELETE \
  --url http://localhost:3333/repositories/${repositoryId}
```

POST /repositories/:id/like
```bash
curl --request POST \
  --url http://localhost:3333/repositories/${repositoryId}/like \
  --header 'content-type: application/json'
```