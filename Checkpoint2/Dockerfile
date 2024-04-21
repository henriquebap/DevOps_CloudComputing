# Imagem oficial do Nginx como base do projeto, tag latest para chamar a última versão
FROM nginx:latest  

RUN apt-get update \
    &&  apt-get install -y curl vim \
    && rm -rf /var/lib/apt/lists/*

# Criando um usuário com UID 97796
RUN useradd -rm -d /home/97796 -s /bin/bash -u 97796 97796 \
    && mkdir /home/97796/meu-site \
    && chown -R 97796:97796 /home/97796

# Copiando os arquivos da página web estática para o diretório padrão do Nginx
COPY ./index.html /usr/share/nginx/html/
COPY ./styles.css /usr/share/nginx/html/
COPY ./tenis.jpg /usr/share/nginx/html/imagem/

# Adicionando metadados através do LABEL
LABEL Imagem="RM97796-NGINX" \
    Autor="97796" \
    Versao="1.0" \
    Descricao="Imagem do Nginx com HTML estático" \
    Email="rm97796@fiap.com.br"

# Porta padrão HTTP 8080
EXPOSE 8080

# CMD (RODAR O WEB SERVER)
CMD ["nginx", "-g", "daemon off;"]
