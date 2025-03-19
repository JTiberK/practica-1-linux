## **Práctica: "Configuración de un Entorno de Desarrollo Básico en Linux"**

### **Nivel:** Básico

### **Objetivo General:**

Configurar un entorno de desarrollo básico en Linux, familiarizándose con comandos fundamentales, el sistema de archivos, gestión de usuarios y automatización de tareas mediante scripting.

---

### **1. Introducción (30 minutos)**

#### **1.1. Objetivos de la práctica**

- Aprender a navegar por el sistema de archivos usando comandos básicos.
- Crear y gestionar archivos y directorios.
- Comprender los permisos de archivos y usuarios.
- Automatizar una tarea simple mediante scripting.

#### **1.2. Herramientas necesarias**

- Acceso a una máquina virtual o contenedor Linux (puedes usar VirtualBox, WSL o Docker).
- Terminal abierta.

**Consejo:** Si no estás seguro de cómo conectarte a tu sistema Linux, consulta la documentación oficial o busca tutoriales sobre `ssh` o WSL.

---

### **2. Actividad 1: Navegación y Manipulación de Archivos (1 hora)**

#### **2.1. Instrucciones**

1. **Exploración del sistema de archivos:**

   - Verifica tu directorio actual. ¿Qué comando puedes usar para esto?

   pwd

   - Lista los archivos y directorios en `/home`. ¿Cómo puedes listarlos de manera detallada (mostrando permisos y tamaño)?

   ls -lh /home

   - Crea un nuevo directorio llamado `practica-linux` dentro de `/tmp`. ¿Qué comando necesitas?

   mkdir /tmp/practica-linux

2. **Manipulación de archivos:**

   - Crea un archivo vacío llamado `config.txt` dentro de `practica-linux`. ¿Cómo lo harías?

   touch /tmp/practica-linux/config.txt

   - Escribe algunas líneas de texto en `config.txt`. ¿Qué comando te permite agregar texto a un archivo?
   - Muestra el contenido del archivo. ¿Cómo puedes hacerlo sin abrir un editor?

3. **Búsqueda de archivos:**
   - Busca todos los archivos `.txt` en `/tmp`. ¿Qué comando puedes usar para buscar archivos específicos?

#### **2.2. Preguntas de reflexión**

- ¿Qué diferencia hay entre `pwd` y `ls`?
- ¿Cómo puedes verificar si un archivo existe antes de intentar modificarlo?

---

### **3. Actividad 2: Gestión de Usuarios y Permisos (1 hora)**

#### **3.1. Instrucciones**

1. **Creación de un usuario:**

   - Crea un usuario llamado `devuser`. Investiga qué comando se usa para crear usuarios y cómo asignarles contraseñas.

2. **Gestión de permisos:**

   - Cambia el propietario de `config.txt` a `devuser`. ¿Qué comando te permite cambiar el propietario de un archivo?
   - Modifica los permisos de `config.txt` para permitir solo lectura. ¿Qué número debes usar con `chmod` para este propósito?

3. **Prueba de permisos:**
   - Intenta editar `config.txt` como el usuario actual. ¿Qué sucede? Luego cambia al usuario `devuser` y vuelve a intentarlo. ¿Cómo puedes cambiar temporalmente de usuario desde la terminal?

#### **3.2. Preguntas de reflexión**

- ¿Qué significa cada columna en la salida de `ls -l`?
- ¿Cómo puedes ver los grupos a los que pertenece un usuario?

---

### **4. Actividad 3: Automatización con Scripts (1 hora)**

#### **4.1. Instrucciones**

1. **Creación del script:**

   - Crea un script llamado `backup.sh` que copie `config.txt` a un directorio de respaldo con una fecha en el nombre del archivo (por ejemplo, `backup_config_20231015.txt`). Investiga cómo usar variables y comandos como `cp` y `date`.

2. **Hacer el script ejecutable:**

   - Cambia los permisos del script para que sea ejecutable. ¿Qué comando necesitas?

3. **Ejecución del script:**

   - Ejecuta tu script y verifica que se haya creado el archivo de respaldo. ¿Cómo puedes asegurarte de que el script funcionó correctamente?

4. **Programación con cron:**
   - Configura una tarea programada para ejecutar tu script cada día a las 8:00 AM. Investiga cómo editar el crontab y el formato de horarios.

#### **4.2. Preguntas de reflexión**

- ¿Qué hace el símbolo `#` al inicio de una línea en un script?
- ¿Cómo puedes probar tu script antes de programarlo con cron?

---

### **5. Evaluación Final**

#### **5.1. Tarea**

Crea un script llamado `info_system.sh` que realice lo siguiente:

1. Muestre la fecha y hora actual.
2. Liste todos los usuarios activos en el sistema.
3. Guarde la salida en un archivo llamado `system_info.txt`.

**Pistas:**

- Para mostrar la fecha y hora, investiga el comando `date`.
- Para listar usuarios activos, busca información sobre el comando `who`.
- Para guardar la salida en un archivo, investiga cómo redirigir la salida de un comando usando `>` o `>>`.

#### **5.2. Revisión**

- Ejecuta tu script y comparte los resultados con el instructor. ¿Funcionó correctamente? ¿Qué problemas encontraste y cómo los resolviste?

---

### **6. Conclusión**

#### **6.1. Resumen**

- Repasa los conceptos clave que aplicaste durante la práctica: navegación, gestión de archivos, permisos y scripting.
- Discute cómo podrías extender estas habilidades para automatizar tareas más complejas en el futuro.

#### **6.2. Reflexión**

- ¿Qué desafíos enfrentaste durante la práctica? ¿Cómo los superaste?
- ¿Cómo podrías aplicar estos conocimientos en proyectos futuros?

---

### **7. Recursos Adicionales**

- Documentación oficial de comandos Linux: `man <comando>`.
- Tutoriales en línea sobre scripting y administración de sistemas.
- Experimenta con otros comandos útiles como `find`, `grep` y `sed`.
