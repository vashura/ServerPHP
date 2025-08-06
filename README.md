# ServerPHP
entorno de desarrollo php

para construir la imagen 
ejecutar el comando
    docker build --file .docker/dockerfile --tag phpsandbox . 

despues ejecutar el comando
    docker run -d -p 80:80 -p 8443:443 --name myphpservercontainer phpsandbox	

para entrar al contenedor ejectuar el comando
    docker exec -it myphpservercontainer bash

para probar la funcionalidad del docker crear el archivo index.php con el comando touch
    touch index.php

modificar el archivo index.php con el contenido

<?php
phpinfo();
?>

y revisar en el navegador
conexion sin ssl: http://localhost 
conexion con ssl:https://localhost:8443