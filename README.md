# TallerObligatorio
Funcionamiento del playbook "webserver.yml"
El playbook mencionado lo que hace es instalar y levantar el servicio apache, configurar y activar el firewall, crear un virtualhost para poder acceder vía web.
Funciona tanto para sistemas operativos redhat como debian.
Los diferencia porque dentro del playbook están vinculados dos roles que hacen referencia a cada sistema.
Los equipos a los cuáles le va a ejecutar las tareas deben estar añadidos con su nombre de equipo e ip en un archivo "inventario" en el mismo directorio donde se encuentra el playbook.

Para ejecutarlo debemos hacerlo con el siguiente comando

ansible-playbook webserver.yml --ask-become-pass

Se verá como en la pantalla muestra el recorrido del playbook por todas sus tareas, devolviendo "OK" en los equipos que realiza correctamente la tarea y "Skipping" en los que no la realizó porque no correspondía
