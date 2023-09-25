## SRI :yum:

## Practica 2

###

**`docker pull httpd`** :arrow_right: descargamos la ultima version de la imagen de Apache

**`docker images`** :arrow_right: comprobamos que la imagen este en nuestro equipo

**`docker run -dit --name asir_httpd -p 8000:80 -v /home/asir2/SRI/apache/paginas httpd:2.4`** :arrow_right: creamos un contenedor con nombre *asir_httpd* con un mapeo de puertos y un volumen asociado al mismo
###
**Ahora hacemos el documento HTML:** 
```
<html>
    <body>
    <p>Hola mundo</p>
    </body>
</html>
```
**`docker run -dit --name asir_web1 -p 8000:80 -v /home/asir2/SRI/apache/paginas httpd:2.4`** :arrow_right: creamos un contenedor con nombre *asir_web1* con un mapeo de puertos y un volumen asociado al mismo

**`docker run -dit --name asir_web2 -p 9080:80 -v /home/asir2/SRI/apache/paginas httpd:2.4`** :arrow_right: creamos un contenedor con nombre *asir_web2* con un mapeo de puertos diferente al primero pero el mismo volumen asociado.

### Una vez hecho esto veremos y comprobaremos si al navegar en las dos direcciones se muestra lo mismo ###

**Las direcciones seran las siguientes:**
```
http://localhost:9080 
http://localhost:8000
```