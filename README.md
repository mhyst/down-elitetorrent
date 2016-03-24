##¿Qué es down?

En realidad debería llamarse EliteTorrent Series Download. Solo que es un nombre poco adecuado para un script de bash. Si quieres lo puedes renombrar a etsdown, o algo así. El renombrarlo no causa problemas. Sirve para mirar en elitetorrent si hay nuevos capítulos de las series que sigues. También los añade a tu programa de torrents. En realidad, el script sólo funciona con Transmission, programa que considero el mejor por muchas cosas. Una de ellas es que permite conectarse de forma remota desde una red local o desde Internet si lo configuras. Y con el comando transmission-remote se puede interactuar. Si has optado por otra solución que permita algo parecido, seguro que no tendrás problema en modificar el script tú mismo para adaptarlo a tu software de torrents.

##Idea tras down

El caso es que mucha gente sigue series viejas o nuevas por torrent. Prácticamente cada día de la semana miramos a ver si está el siguiente capítulo de nuestro programa favorito en elitetorrent. Aunque sólo mires una vez al día la página, pinchar y añadir los torrents puede ser un trabajo considerable en tiempo. Si lo haces demasiadas veces a la semana, se convierte en una rutina molesta. Y pensé yo, ¿qué me impide escribir un script que haga justamente eso por mi? La respuesta fue: absolutamente nada. Hoy en día hay herramientas de ayer, hoy y siempre; que nos pueden hacer la vida muy fácil. Bash scripting es una de esas cosas. 

Así que ¿qué hace exactamente down? Muy simple. Descarga la página de series, extrae cada epispdio de la página y comprueba si nuestra copia de Transmission ya tiene cada torrent. Cuando se encuentra uno que no tiene, visita su página, consigue el magnet y lo añade a Transmission. 

El comando no requiere de argumentos. Se puede programar con cron a una hora determinada del día.