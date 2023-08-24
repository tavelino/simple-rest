Para realizar a instação da aplicação é necessário criar um projeto.

```
oc new-project simple-api
```

Após criar o projeto, é necessário realizar o deploy da aplicação, utilizando o s2i para realizar a varredura do projeto no github e gerar a criação da imagem e os componentes de deploy (deployment, service, build ...) podemos realizar o deploy da seguinte forma.

```
oc new-app --name simple-api https://github.com/tavelino/simple-rest#main --strategy=source
```

Em seguida é necessário expor a aplicação para acesso externo. Utilizamos o comando ´expose´ para isso.

```
oc expose svc simple-api
```
