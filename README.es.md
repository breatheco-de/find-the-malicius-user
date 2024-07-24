# Encuentra al Usuario Malicioso

Descarga la siguiente [máquina virtual con Ubuntu Server](https://storage.googleapis.com/breathecode/virtualbox/Ubuntu-Server-Find-Malicious-User.ova) y ejecuta la computadora en Virtual Box en tu ordenador.

Acabas de unirte al equipo de ciberseguridad de 4Geeks Academy. El equipo está actualmente configurando un servidor web con Ubuntu para la plataforma de E-Learning. Este equipo está compuesto por:

1. Alejandro
2. Daniela
3. Vanessa
4. Chema
5. Analista (Tú)

Tu contraseña y usuario es:

```bash
usuario: analista
contraseña: analista
```

Cada usuario tiene sus propios directorios y archivos, así como algunos compartidos, con diferentes permisos sobre los archivos compartidos. Uno de estos usuarios tiene permisos que no debería tener y parece que está tramando algo. ¿Puedes descubrir quién es?

1. Identifica al usuario malicioso
2. Analiza sus acciones y explica qué intentaba hacer
3. Determina qué permisos tenía y sobre qué directorios que le permitían ejecutar esta acción
4. Propón una solución a este problema
> ⚠️ El permiso Sticky bit (rwx-t) se usa a menudo para otorgar acceso selectivo a archivos y directorios.


## 💡 AYUDA

- La maquina Ubuntu que hemos diseñado para ti no tiene interfaz gráfica porque además de probar tus habilidades de hacking queremos también probar tus habilidades con la linea de comando. 
- El sistema de directorios principal donde vas a estar investigando activamente es el siguiente:

```bash
|- home
    |-alejandro
    |-analista
    |-chema
    |-daniela
    |-vanessa
    |-vboxuser
```
> ⚠️ Al iniciar sesion vas a estar posicionado en el directorio `./analista`

- En el directorio `./home` se encuentran las primeras instrucciones.

