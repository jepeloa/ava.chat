# Ava chatbot

1-Generar cerfificados SSL. Copiarlos a la carpeta certs del raiz del proyecto. Se deben llamar fullchain.pem y privkey.pem, yo use letsencrypt

2-En en archivo nginx.con en la linea server_name tu_dominio.com;  poner el nombre de dominio que apuntan los certificados.

3-dentro de el archivo env.example cargar la configuracion de login de google (requiere ID de cliente y Secret)

4-Renombrar el archivo env.example a .env

5-Docker compose up -d --build en el raiz del proyecto

El docker file este levanta tanto backend como frontend. El frontend lo compila por lo que va a demorar su tiempo (media hora o mas en levantar todo depende los recuros de la maquina).

6-Cuando termina en la direccion https://tudominio.com deberia estar listo para probarse.
