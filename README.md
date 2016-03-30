##¿Qué es down?

En realidad debería llamarse EliteTorrent Series Download. Solo que es un nombre poco adecuado para un script de bash. Si quieres lo puedes renombrar a etsdown, o algo así. El renombrarlo no causa problemas. Sirve para mirar en elitetorrent si hay nuevos capítulos de las series que sigues. También los añade a tu programa de torrents. En realidad, el script sólo funciona con Transmission, programa que considero el mejor por muchas cosas. Una de ellas es que permite conectarse de forma remota desde una red local o desde Internet si lo configuras. Y con el comando transmission-remote se puede interactuar. Si has optado por otra solución que permita algo parecido, seguro que no tendrás problema en modificar el script tú mismo para adaptarlo a tu software de torrents.

##Idea tras down

El caso es que mucha gente sigue series viejas o nuevas por torrent. Prácticamente cada día de la semana miramos a ver si está el siguiente capítulo de nuestro programa favorito en elitetorrent. Aunque sólo mires una vez al día la página, pinchar y añadir los torrents puede ser un trabajo considerable en tiempo. Si lo haces demasiadas veces a la semana, se convierte en una rutina molesta. Y pensé yo, ¿qué me impide escribir un script que haga justamente eso por mi? La respuesta fue: absolutamente nada. Hoy en día hay herramientas de ayer, hoy y siempre; que nos pueden hacer la vida muy fácil. Bash scripting es una de esas cosas. 

Así que ¿qué hace exactamente down? Muy simple. Descarga la página de series, extrae cada epispdio de la página y comprueba si nuestra copia de Transmission ya tiene cada torrent. Cuando se encuentra uno que no tiene, visita su página, consigue el magnet y lo añade a Transmission. 

El comando no requiere de argumentos. Se puede programar con cron a una hora determinada del día.

##Cómo indicar las series que seguimos

down sigue la misma estrategia que clat. Se necesita un directorio que contenga archivos cuyos nombres coincidan cada uno con el de una serie. La comparación tiene en cuenta mayúsculas y minúsculas. Asegurate que los nombres coinciden con los de las series en elitetorrent.

Antes de ejecutar el script hay que abrirlo y modificar las variables SERVER y DIR.
SERVER contiene un fragmento necesario para la linea de comandos de transmission-remote. La dirección IP del ordenador donde está Transmission, el puerto, y si en la configuración de Transmission hemos elegido introducir usuario y contraseña, estos deberán añadirse también detrás de --auth, sustituyendo admin:admin por lo que hayas elegido poner. DIR contiene la ruta hacia el directorio en el que se guardan los archivos con los nombres de tus series, como decíamos en el párrafo anterior. Una vez cambiadas esas dos variables, ya sólo nos queda comprobar la conexión a Internet y escribir down en una terminal.

## Opciones

* La forma más sencilla es sin opciones. Descargará la página de la sección de series sin necesidad de ningún argumento.

* Si ponemos algún argumento, down entenderá que debe buscarlo en elitetorrent. Para que tenga éxito el argumento debe coincidir con el título de alguna serie o película.

* Si como primer parámetro ponemos -u, a continuación podemos pasarle la url que queramos. Para que funcione deberá tener la misma estructura de elitetorrent. Por ejemplo podemos facilitarle una página concreta del mismo elitetorrent con episodios o películas que queramos añadir a Transmission para descargar. De esa forma podremos descargar episodios o películas que no estén en los índices generales de la web.