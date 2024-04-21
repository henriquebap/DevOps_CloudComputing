## Docker - Chekpoint 2 - NGINX

#### Construção de Docker com NGINX como base

##### Hospedar uma Pagina web estatica em um container, com css e HTML

---

## Aluno:

- Henrique Baptista - RM97796

---

Obs: verifique se esta no caminho correto do arquivo Docker

```
docker build -t 97796-nginx .
```

```
docker run -d --name 97796-nginx-container -p 8080:80 97796-nginx
```
