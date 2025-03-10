Dos versiones para realizar la tarea:

  v1:
  # Docker Compose que monta 4 contenedores-servicios:
  #   - Contenedor httpd-alpine (mas liviano) (puerto 80) con servicio web apache. Archivos http.conf y http-vhosts.conf modificados para recibir php.
  #   - Contenedor mysql (puerto 3306) con base de datos para Wordpress y Proyecto. Se agrega script para crear y rellenar la base de datos de Proyecto.
  #   - Contenedor phpmyadmin (puerto 8080) que va a permitir el acceso mediante interfaz grafica web a las bbdd-s (root, deaw, word).
  #   - Contenedor wordpress-fpm (preconfigurado para com. con servidor web) con instalacion a iniciar (puerto 80) y descarga mediante github de carpeta Proyecto
  # Volumenes:
  #   - php_data: Comparte los datos de wordpres y proyecto entre cont. httpd y wordpress.
  # Autor:
  #   - Jose Maria Garcia Conde / DEAW04-TE02 / 24-25

  v2:
  # Docker Compose que monta 3 contenedores-servicios:
  #   - Contenedor mysql (puerto 3306) con base de datos para Wordpress y Proyecto. Se agrega script para crear y rellenar la base de datos de Proyecto.
  #   - Contenedor phpmyadmin (puerto 8080) que va a permitir el acceso mediante interfaz grafica web a las bbdd-s (root, deaw, word).
  #   - Contenedor web wordpress (puerto 80) con instalacion a iniciar y descarga mediante github de carpeta Proyecto
  # Volumenes:
  #   - No se usan ya que el cont. wordpress hace de web-server. (luego se autogeneran)
  # Autor:
  #   - Jose Maria Garcia Conde / DEAW04-TE02 / 24-25
