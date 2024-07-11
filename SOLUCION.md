Para abordar este proyecto de ciberseguridad en el equipo de 4Geeks Academy, seguiría un enfoque metódico y estructurado para identificar y resolver el problema del usuario malicioso. Aquí tienes un paso a paso detallado:

### 1. **Recopilación de Información Inicial**

- **Acceso a Logs y Auditorías**: Comenzaría solicitando acceso a todos los registros de auditoría y logs del sistema del servidor Ubuntu. Esto incluye logs de acceso, logs de cambios en permisos, y cualquier otro log relevante (por ejemplo, `/var/log/auth.log`, `/var/log/syslog`, y logs específicos de la aplicación).

- **Revisión de Permisos Actuales**: Haría una revisión completa de los permisos actuales de cada usuario (Alejandro, Daniela, Vanessa, Chema, y el Analista) sobre los diferentes directorios y archivos.

### 2. **Análisis de Logs y Movimientos**

- **Filtrado de Actividades Sospechosas**: Analizaría los logs en busca de actividades inusuales, como intentos de acceso fuera del horario normal, múltiples intentos fallidos de autenticación, y comandos ejecutados que podrían modificar permisos o acceder a datos sensibles.

- **Comparación de Actividades**: Compararía los patrones de comportamiento de cada usuario con sus roles y responsabilidades. Por ejemplo, Chema podría tener más acceso a herramientas de seguridad, mientras que Daniela podría estar más centrada en el desarrollo de la plataforma.

### 3. **Identificación del Usuario Malicioso**

- **Identificación de Permisos Incorrectos**: Revisaría los permisos en los directorios y archivos comunes para identificar a los usuarios con permisos excesivos o inapropiados. Esto se puede hacer utilizando comandos como `ls -l` y `getfacl`.

- **Correlación con Logs**: Correlacionaría las actividades sospechosas encontradas en los logs con los usuarios que tienen permisos inapropiados. Esto podría ayudar a identificar al usuario que está intentando realizar actividades maliciosas.

### 4. **Análisis de Intenciones**

- **Revisión de Comandos Ejecutados**: Analizaría los comandos ejecutados por el usuario sospechoso para entender qué intentaba hacer. Por ejemplo, si el usuario ejecutó comandos para copiar datos sensibles o modificar archivos de configuración.

- **Entrevistas y Confirmación**: Podría entrevistar al equipo para obtener más contexto sobre las actividades recientes y confirmar si algún usuario ha reportado problemas de acceso o comportamiento inusual.

### 5. **Permisos Inapropiados y Acciones Ejecutadas**

- **Permisos Identificados**: Documentaría los permisos específicos que el usuario malicioso tenía y sobre qué directorios. Esto incluiría permisos de lectura, escritura, y ejecución.

- **Acciones Maliciosas**: Describiría las acciones específicas que el usuario pudo realizar gracias a esos permisos. Por ejemplo, acceso a directorios de configuración, copia de datos sensibles, o modificación de scripts críticos.

### 6. **Resolución del Problema**

- **Revocación de Permisos**: Inmediatamente revocaría los permisos inapropiados del usuario identificado. Esto se puede hacer utilizando comandos como `chmod` y `chown` para modificar los permisos y propietarios de los archivos y directorios.

- **Actualización de Políticas de Seguridad**: Implementaría políticas más estrictas de control de acceso y permisos, asegurando que cada usuario solo tenga los permisos mínimos necesarios para realizar su trabajo.

- **Monitoreo Continuo**: Configuraría herramientas de monitoreo y alertas para detectar actividades sospechosas en tiempo real. Esto podría incluir el uso de herramientas como `auditd` y `ossec`.

- **Capacitación del Equipo**: Proporcionaría capacitación adicional al equipo sobre buenas prácticas de seguridad y la importancia de seguir las políticas de acceso y permisos.

### Conclusión

Con este enfoque metódico, podríamos identificar al usuario malicioso, analizar sus movimientos, entender sus intenciones, y tomar medidas correctivas para asegurar que el sistema sea seguro y los permisos estén correctamente gestionados. Este proceso también ayuda a fortalecer la postura de seguridad del equipo y prevenir futuros incidentes.
