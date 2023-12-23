FROM debian:latest
LABEL autor="fcuadradoa01@educantabria.es"
LABEL version="1.0"
LABEL description="trabajando con imagenes personalizadas" 
# instalamos apache2 
RUN apt-get update && apt-get install -y apache2 
# limpio cache 
RUN apt-get clean && rm -rf /var/lib/apt/lists/* 
# abro puerto 
EXPOSE 80 
# cargo pagina de inicio (como no especifico ruta se asume que esta en la misma carpeta) 
COPY index.html /var/www/html/ 
# arranco el servicio 
ENTRYPOINT ["apachectl", "-D", "FOREGROUND"]
