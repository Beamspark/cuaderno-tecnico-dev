[← Volver al Índice de PACs](./index.md)

---

# PAC 1 (RA4) - Administración de Sistemas Operativos Propietarios

---

### Pregunta 1
En un ordenador con Windows, ¿qué tipo de cuenta es recomendable para realizar tareas cotidianas sin disponer de privilegios administrativos?

<details class="quiz-option incorrect">
  <summary>A) Una cuenta de superusuario root.</summary>
  <div class="feedback">
    <div class="feedback-title">✗ Incorrecto</div>
    La cuenta <code>root</code> es propia de sistemas operativos tipo UNIX/Linux y, además, posee privilegios totales sobre el sistema.
  </div>
</details>

<details class="quiz-option correct">
  <summary>B) Una cuenta de usuario estándar</summary>
  <div class="feedback">
    <div class="feedback-title">✓ ¡Exacto!</div>
    Siguiendo el <strong>principio de mínimo privilegio</strong>, el uso diario de una cuenta estándar permite ejecutar aplicaciones y gestionar archivos personales impidiendo que cambios accidentales o código malicioso modifiquen archivos críticos del sistema o instalen software sin elevar permisos mediante el Control de Cuentas de Usuario (UAC).
  </div>
</details>

<details class="quiz-option incorrect">
  <summary>C) Una cuenta con control total sobre el sistema.</summary>
  <div class="feedback">
    <div class="feedback-title">✗ Incorrecto</div>
    El control total equivale a privilegios administrativos máximos, lo cual incrementa innecesariamente la superficie de ataque en el uso cotidiano.
  </div>
</details>

<details class="quiz-option incorrect">
  <summary>D) Una cuenta de administrador.</summary>
  <div class="feedback">
    <div class="feedback-title">✗ Incorrecto</div>
    Las cuentas de administrador deben reservarse únicamente para tareas puntuales de configuración, mantenimiento o instalación de programas en el equipo.
  </div>
</details>

---

### Pregunta 2
¿Qué prepara Windows automáticamente cuando un nuevo usuario inicia sesión por primera vez?

<details class="quiz-option incorrect">
  <summary>A) Una copia completa del disco.</summary>
  <div class="feedback">
    <div class="feedback-title">✗ Incorrecto</div>
    El inicio de sesión no genera copias de seguridad ni clonaciones de volumen.
  </div>
</details>

<details class="quiz-option incorrect">
  <summary>B) Una reinstalación del sistema operativo.</summary>
  <div class="feedback">
    <div class="feedback-title">✗ Incorrecto</div>
    El sistema operativo ya está instalado; únicamente inicializa el entorno personalizado del nuevo usuario.
  </div>
</details>

<details class="quiz-option correct">
  <summary>C) El perfil de usuario.</summary>
  <div class="feedback">
    <div class="feedback-title">✓ ¡Exacto!</div>
    Al primer inicio de sesión, Windows crea la estructura de directorios personales en <code>C:\Users\&lt;Usuario&gt;</code> (Escritorio, Documentos, Descargas, <code>AppData</code>) y genera su archivo de configuración individual del registro (<code>NTUSER.DAT</code>) a partir de la plantilla <code>Default</code>.
  </div>
</details>

<details class="quiz-option incorrect">
  <summary>D) Una nueva partición de arranque.</summary>
  <div class="feedback">
    <div class="feedback-title">✗ Incorrecto</div>
    Las particiones del disco se definen durante la instalación o mediante el Administrador de discos, no al crear o iniciar sesiones de usuario.
  </div>
</details>

---

### Pregunta 3
Un alumno elimina un archivo desde el Explorador y este permanece en la Papelera de reciclaje. ¿Cómo puede recuperarlo?

<details class="quiz-option incorrect">
  <summary>A) Creando un acceso directo con el mismo nombre.</summary>
  <div class="feedback">
    <div class="feedback-title">✗ Incorrecto</div>
    Un acceso directo solo apunta a una ruta, pero no restaura el contenido ni los metadatos del fichero eliminado.
  </div>
</details>

<details class="quiz-option incorrect">
  <summary>B) Cambiando el nombre de su cuenta.</summary>
  <div class="feedback">
    <div class="feedback-title">✗ Incorrecto</div>
    Modificar el nombre de usuario no afecta al estado de los archivos almacenados en <code>$Recycle.Bin</code>.
  </div>
</details>

<details class="quiz-option incorrect">
  <summary>C) Reiniciando el ordenador y entrando al directorio donde se encontraba ubicado</summary>
  <div class="feedback">
    <div class="feedback-title">✗ Incorrecto</div>
    Mientras no se restaure desde la Papelera, el archivo permanece movido en el contenedor oculto del sistema y no aparece en su carpeta original.
  </div>
</details>

<details class="quiz-option correct">
  <summary>D) Seleccionando la opción «Restaurar» en la papelera.</summary>
  <div class="feedback">
    <div class="feedback-title">✓ ¡Exacto!</div>
    Al hacer clic derecho sobre el elemento dentro de la Papelera de reciclaje y pulsar <strong>Restaurar</strong>, Windows devuelve el archivo exactamente a la ruta original desde la que fue eliminado.
  </div>
</details>

---

### Pregunta 4
¿Qué comando abre la consola de administración de servicios de Windows?

<details class="quiz-option correct">
  <summary>A) services.msc</summary>
  <div class="feedback">
    <div class="feedback-title">✓ ¡Exacto!</div>
    Ejecutar <code>services.msc</code> (desde el cuadro <em>Ejecutar</em> <code>Win + R</code> o consola) abre el complemento gráfico de <em>Microsoft Management Console</em> encargado de iniciar, detener, reiniciar y configurar el tipo de arranque de los servicios del sistema.
  </div>
</details>

<details class="quiz-option incorrect">
  <summary>B) regedit</summary>
  <div class="feedback">
    <div class="feedback-title">✗ Incorrecto</div>
    Abre el Editor del Registro de Windows, no la consola de servicios.
  </div>
</details>

<details class="quiz-option incorrect">
  <summary>C) winver</summary>
  <div class="feedback">
    <div class="feedback-title">✗ Incorrecto</div>
    Muestra una ventana informativa con la versión exacta y compilación de Windows instalada.
  </div>
</details>

<details class="quiz-option incorrect">
  <summary>D) systemctl</summary>
  <div class="feedback">
    <div class="feedback-title">✗ Incorrecto</div>
    Es la utilidad de gestión de servicios (<code>systemd</code>) propia de distribuciones GNU/Linux, inexistente de forma nativa en Windows.
  </div>
</details>

---

### Pregunta 5
¿Qué consecuencia tiene detener el servicio «Cola de impresión» de Windows?

<details class="quiz-option incorrect">
  <summary>A) Se borran todos los documentos del usuario activo</summary>
  <div class="feedback">
    <div class="feedback-title">✗ Incorrecto</div>
    Los archivos personales del usuario no se eliminan al detener el servicio; únicamente se interrumpe la gestión de trabajos hacia las impresoras.
  </div>
</details>

<details class="quiz-option incorrect">
  <summary>B) Se eliminan las impresoras conectadas</summary>
  <div class="feedback">
    <div class="feedback-title">✗ Incorrecto</div>
    Las impresoras y sus controladores siguen instalados en el sistema, aunque dejan de mostrarse o estar operativas hasta volver a iniciar el servicio.
  </div>
</details>

<details class="quiz-option correct">
  <summary>C) El equipo deja de gestionar trabajos de impresión mientras el servicio está detenido.</summary>
  <div class="feedback">
    <div class="feedback-title">✓ ¡Exacto!</div>
    El servicio <strong>Cola de impresión</strong> (<code>Spooler</code>) almacena temporalmente en disco (<code>C:\Windows\System32\spool\PRINTERS</code>) y envía los documentos a las impresoras; al detenerlo, el equipo no puede procesar ni enviar nuevas impresiones hasta que se reactive.
  </div>
</details>

<details class="quiz-option incorrect">
  <summary>D) Se cierra automáticamente la sesión de usuario abierta</summary>
  <div class="feedback">
    <div class="feedback-title">✗ Incorrecto</div>
    La detención del <em>Print Spooler</em> no afecta al subsistema de inicio de sesión ni cierra la sesión activa.
  </div>
</details>

---

### Pregunta 6
¿Qué comando de PowerShell muestra los servicios de Windows y su estado?

<details class="quiz-option incorrect">
  <summary>A) Get-Process</summary>
  <div class="feedback">
    <div class="feedback-title">✗ Incorrecto</div>
    Lista los procesos activos en ejecución en la memoria del sistema, no los servicios registrados.
  </div>
</details>

<details class="quiz-option incorrect">
  <summary>B) Start-Service</summary>
  <div class="feedback">
    <div class="feedback-title">✗ Incorrecto</div>
    Se utiliza para arrancar uno o varios servicios detenidos, no para consultar su listado y estado.
  </div>
</details>

<details class="quiz-option correct">
  <summary>C) Get-Service</summary>
  <div class="feedback">
    <div class="feedback-title">✓ ¡Exacto!</div>
    El cmdlet <code>Get-Service</code> devuelve el listado de servicios instalados en el equipo local o remoto indicando su estado actual (<code>Running</code> o <code>Stopped</code>), nombre interno (<code>Name</code>) y nombre para mostrar (<code>DisplayName</code>).
  </div>
</details>

<details class="quiz-option incorrect">
  <summary>D) Stop-Service</summary>
  <div class="feedback">
    <div class="feedback-title">✗ Incorrecto</div>
    Sirve para detener un servicio que se encuentra en ejecución.
  </div>
</details>

---

### Pregunta 7
¿Qué comando de PowerShell permite iniciar el servicio Cola de impresión?

<details class="quiz-option incorrect">
  <summary>A) Get-Process Spooler</summary>
  <div class="feedback">
    <div class="feedback-title">✗ Incorrecto</div>
    Busca un proceso llamado <em>Spooler</em>, pero no inicia ningún servicio del sistema.
  </div>
</details>

<details class="quiz-option correct">
  <summary>B) Start-Service Spooler</summary>
  <div class="feedback">
    <div class="feedback-title">✓ ¡Exacto!</div>
    Dado que el nombre interno del servicio <em>Cola de impresión</em> en Windows es <code>Spooler</code>, ejecutar <code>Start-Service Spooler</code> (o <code>Start-Service -Name Spooler</code>) con permisos de administrador lo pone en marcha inmediatamente.
  </div>
</details>

<details class="quiz-option incorrect">
  <summary>C) Stop-Service Spooler</summary>
  <div class="feedback">
    <div class="feedback-title">✗ Incorrecto</div>
    Realiza la acción inversa: detiene el servicio <code>Spooler</code>.
  </div>
</details>

<details class="quiz-option incorrect">
  <summary>D) Get-Service Spooler</summary>
  <div class="feedback">
    <div class="feedback-title">✗ Incorrecto</div>
    Únicamente consulta y muestra el estado actual del servicio sin modificarlo.
  </div>
</details>

---

### Pregunta 8
¿Qué significa configurar un servicio de Windows con inicio «Automático (inicio retrasado)»?

<details class="quiz-option incorrect">
  <summary>A) Que solo podrá iniciarse manualmente.</summary>
  <div class="feedback">
    <div class="feedback-title">✗ Incorrecto</div>
    Esa conducta corresponde al modo de inicio <strong>Manual</strong>.
  </div>
</details>

<details class="quiz-option correct">
  <summary>B) Que se iniciará después del arranque inicial para reducir la carga de ese momento.</summary>
  <div class="feedback">
    <div class="feedback-title">✓ ¡Exacto!</div>
    El modo <strong>Automático (inicio retrasado)</strong> pospone el arranque de servicios no críticos (como Windows Update o Windows Search) unos instantes después de que hayan cargado los servicios esenciales del sistema, agilizando el inicio de Windows y evitando cuellos de botella de CPU y disco.
  </div>
</details>

<details class="quiz-option incorrect">
  <summary>C) Que se detendrá automáticamente al abrir una aplicación</summary>
  <div class="feedback">
    <div class="feedback-title">✗ Incorrecto</div>
    El inicio retrasado regula cuándo arranca el servicio tras encender el equipo, no su detención al abrir programas.
  </div>
</details>

<details class="quiz-option incorrect">
  <summary>D) Que no podrá iniciarse hasta reinstalar Windows.</summary>
  <div class="feedback">
    <div class="feedback-title">✗ Incorrecto</div>
    El servicio arranca de forma totalmente normal y automática en cada encendido, solo que diferido unos segundos respecto a los servicios críticos.
  </div>
</details>

---

### Pregunta 9
¿Qué herramienta permite consultar la base de datos de configuración de Windows?

<details class="quiz-option incorrect">
  <summary>A) Windows Update</summary>
  <div class="feedback">
    <div class="feedback-title">✗ Incorrecto</div>
    Gestiona la descarga e instalación de parches y actualizaciones del sistema operativo.
  </div>
</details>

<details class="quiz-option incorrect">
  <summary>B) Administrador de tareas</summary>
  <div class="feedback">
    <div class="feedback-title">✗ Incorrecto</div>
    Supervisa procesos activos, rendimiento de hardware, aplicaciones de inicio y usuarios conectados.
  </div>
</details>

<details class="quiz-option incorrect">
  <summary>C) Administrador de discos</summary>
  <div class="feedback">
    <div class="feedback-title">✗ Incorrecto</div>
    Permite gestionar unidades físicas, particiones, volúmenes y letras de unidad.
  </div>
</details>

<details class="quiz-option correct">
  <summary>D) El Editor del Registro.</summary>
  <div class="feedback">
    <div class="feedback-title">✓ ¡Exacto!</div>
    El <strong>Editor del Registro</strong> (<code>regedit.exe</code>) permite visualizar y modificar la base de datos jerárquica donde Windows y sus aplicaciones almacenan parámetros de configuración de hardware, software, políticas y perfiles de usuario.
  </div>
</details>

---

### Pregunta 10
¿Qué rama del Registro de Windows contiene la configuración del usuario que ha iniciado sesión?

<details class="quiz-option incorrect">
  <summary>A) HKEY_CLASSES_ROOT</summary>
  <div class="feedback">
    <div class="feedback-title">✗ Incorrecto</div>
    Almacena las asociaciones de extensiones de archivo y registros de objetos COM/OLE del sistema.
  </div>
</details>

<details class="quiz-option correct">
  <summary>B) HKEY_CURRENT_USER</summary>
  <div class="feedback">
    <div class="feedback-title">✓ ¡Exacto!</div>
    La rama raíz <strong><code>HKEY_CURRENT_USER</code> (HKCU)</strong> contiene los ajustes personalizados del perfil activo que ha iniciado sesión (fondo de pantalla, variables de entorno de usuario, preferencias de aplicaciones y red), enlazando dinámicamente con su subclave correspondiente dentro de <code>HKEY_USERS</code>.
  </div>
</details>

<details class="quiz-option incorrect">
  <summary>C) HKEY_CURRENT_CONFIG</summary>
  <div class="feedback">
    <div class="feedback-title">✗ Incorrecto</div>
    Recoge información sobre el perfil de hardware activo utilizado durante el arranque actual del equipo.
  </div>
</details>

<details class="quiz-option incorrect">
  <summary>D) HKEY_LOCAL_MACHINE</summary>
  <div class="feedback">
    <div class="feedback-title">✗ Incorrecto</div>
    Guarda la configuración global del equipo (controladores, servicios, software instalado y seguridad) aplicable a todos los usuarios de la máquina.
  </div>
</details>
