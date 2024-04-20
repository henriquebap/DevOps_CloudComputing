# Imagem oficial do Nginx como base do projeto, tag latest para chamar a ultima versao
FROM nginx:latest  

RUN apt-get update \
    &&  apt-get install -y curl vim \
    && rm -rf /var/lib/apt/lists/*

# Criando uma pasta raiz do container chamada meu-site
RUN mkdir /meu-site

# Copiando os arquivos da pagina web estatica para o diretorio padrao do Nginx
COPY ./index.html /usr/share/nginx/html/


# Adicionando meta datos atraves do LABEL
LABEL description="Imagem do Nginx com página estática" \
    maintainer="Henrique Baptista <rm97796@fiap.com.br>"

# porta padrão HTTP 8080
EXPOSE 8080


# CMD (RODAR O WEB SERVER)
CMD ["nginx", "-g", "daemon off;"]