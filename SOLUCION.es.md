Para abordar este proyecto de ciberseguridad en el equipo de 4Geeks Academy, seguiría un enfoque metódico y estructurado para identificar y resolver el problema del usuario malicioso. Aquí tienes un paso a paso detallado:

### 1. Revisión de permisos actuales

- Revisa los permisos de cada uno de los usuarios en detalle, incluyendo directorios y archivos compartidos.

```bash
ls -l /home/alejandro 
ls -l /home/daniela 
```

### 2. Analiza los Logs y movimientos.

- Busca actividades sospechosas en los logs de autenticación y del sistema para identificar patrones de comportamiento inusuales. Usa getfacl para revisar los permisos ACL (Access Control List) en los directorios y archivos comunes de cada usuario. Ejemplo:

```bash
sudo getfacl /daniela
sudo getfacl /analista
```
- Correlaciona las actividades sospechosas encontradas en los logs con los usuarios que tienen permisos inapropiados. Esto podría ayudar a identificar al usuario que está intentando realizar actividades maliciosas.


### 3. Identifica las acciones maliciosas

- Revisa los comandos ejecutados por los usuarios para entender sus intenciones. Puedes usar el comando history para ver el historial de comandos de cada usuario. Ejemplo: 

```bash
sudo -u vanessa history
```

### 4. Revocación de Permisos y reporte de pruebas

- Una vez que identificas el usuario malicioso revoca sus permisos de root usando chmod y chown. Ejemplo:

```bash
sudo chmod 700 /home/analista
sudo chown analista:analista /home/analista
```

- Reune las pruebas en contra del usuario malicioso y protege los archivos con el permiso especial `sticky bit` para que el usuario malicioso  no los pueda tocar.



### Conclusión

Con este enfoque metódico, podríamos identificar al usuario malicioso, analizar sus movimientos, entender sus intenciones, y tomar medidas correctivas para asegurar que el sistema sea seguro y los permisos estén correctamente gestionados. Este proceso también ayuda a fortalecer la postura de seguridad del equipo y prevenir futuros incidentes.
