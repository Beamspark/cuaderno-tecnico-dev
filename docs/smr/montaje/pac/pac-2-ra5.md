[← Volver al Índice de PACs](./index.md)

---

# PAC 2 (RA5) - Instalaciones II

---

### Pregunta 1
¿Qué formato suelen tener las imágenes de disco?

<details class="quiz-option incorrect">
  <summary>A) .doc</summary>
  <div class="feedback">
    <div class="feedback-title">✗ Incorrecto</div>
    Corresponde al formato clásico de documentos de texto de Microsoft Word, ajeno a la encapsulación de sistemas de archivos o soportes ópticos.
  </div>
</details>

<details class="quiz-option incorrect">
  <summary>B) .mp3</summary>
  <div class="feedback">
    <div class="feedback-title">✗ Incorrecto</div>
    Es un formato de compresión de audio digital con pérdida (MPEG-1 Audio Layer III).
  </div>
</details>

<details class="quiz-option correct">
  <summary>C) .iso</summary>
  <div class="feedback">
    <div class="feedback-title">✓ ¡Exacto!</div>
    El formato <strong><code>.iso</code></strong> (basado en el estándar internacional ISO 9660 / UDF) encapsula en un único fichero la copia exacta sector por sector de un disco óptico o medio de instalación arrancable, manteniendo intacta su estructura de directorios y su sector de arranque (<em>El Torito</em>).
  </div>
</details>

<details class="quiz-option incorrect">
  <summary>D) .exe</summary>
  <div class="feedback">
    <div class="feedback-title">✗ Incorrecto</div>
    Es la extensión estándar de los archivos binarios ejecutables en entornos Windows/DOS.
  </div>
</details>

---

### Pregunta 2
¿Qué debe hacerse antes de crear un punto de restauración?

<details class="quiz-option incorrect">
  <summary>A) Desconectar el teclado y ratón.</summary>
  <div class="feedback">
    <div class="feedback-title">✗ Incorrecto</div>
    Los periféricos de entrada no interfieren con la creación de instantáneas del sistema (*Volume Shadow Copy*).
  </div>
</details>

<details class="quiz-option incorrect">
  <summary>B) Borrar todos los datos del disco duro.</summary>
  <div class="feedback">
    <div class="feedback-title">✗ Incorrecto</div>
    Formatear o borrar la unidad eliminaría el propio sistema operativo y el espacio asignado a las instantáneas de restauración.
  </div>
</details>

<details class="quiz-option incorrect">
  <summary>C) Apagar el equipo.</summary>
  <div class="feedback">
    <div class="feedback-title">✗ Incorrecto</div>
    Los puntos de restauración se generan en caliente con el sistema operativo iniciado mediante el servicio de Instantáneas de volumen (VSS).
  </div>
</details>

<details class="quiz-option correct">
  <summary>D) Instalar programas y asegurarse de que el equipo funcione bien.</summary>
  <div class="feedback">
    <div class="feedback-title">✓ ¡Exacto!</div>
    Un punto de restauración guarda una instantánea del estado del Registro de Windows, controladores y archivos críticos del sistema; por ello debe crearse cuando el equipo se encuentra en un estado limpio, estable y operativo (o justo antes de instalar software/controladores críticos que puedan desestabilizarlo).
  </div>
</details>

---

### Pregunta 3
¿Qué es una imagen de disco?

<details class="quiz-option incorrect">
  <summary>A) Un dibujo del disco duro.</summary>
  <div class="feedback">
    <div class="feedback-title">✗ Incorrecto</div>
    El término <em>imagen</em> hace referencia a una réplica lógica bit a bit, no a una representación gráfica.
  </div>
</details>

<details class="quiz-option incorrect">
  <summary>B) Una herramienta para eliminar virus.</summary>
  <div class="feedback">
    <div class="feedback-title">✗ Incorrecto</div>
    Esa función corresponde a software antimalware o soluciones EDR.
  </div>
</details>

<details class="quiz-option incorrect">
  <summary>C) Un archivo en formato .txt.</summary>
  <div class="feedback">
    <div class="feedback-title">✗ Incorrecto</div>
    Los ficheros <code>.txt</code> almacenan exclusivamente texto plano sin formato.
  </div>
</details>

<details class="quiz-option correct">
  <summary>D) Una copia exacta del contenido del disco.</summary>
  <div class="feedback">
    <div class="feedback-title">✓ ¡Exacto!</div>
    Una <strong>imagen de disco</strong> es un fichero único que replica con exactitud la estructura completa y los datos de un volumen o dispositivo de almacenamiento (incluyendo tablas de particiones, sectores de arranque, sistema operativo, programas instalados y configuraciones), permitiendo su clonación o restauración íntegra.
  </div>
</details>

---

### Pregunta 4
¿Qué es una partición en un disco duro?

<details class="quiz-option incorrect">
  <summary>A) Un tipo de cable.</summary>
  <div class="feedback">
    <div class="feedback-title">✗ Incorrecto</div>
    La interconexión física de unidades de almacenamiento se realiza mediante buses o interfaces como SATA, SAS o PCIe/NVMe.
  </div>
</details>

<details class="quiz-option correct">
  <summary>B) Un espacio para guardar datos.</summary>
  <div class="feedback">
    <div class="feedback-title">✓ ¡Exacto!</div>
    Una <strong>partición</strong> es una división lógica definida dentro de la tabla de particiones (MBR o GPT) de una unidad física de almacenamiento. El sistema operativo la gestiona como un volumen independiente (con su propio sistema de archivos como NTFS, ext4 o FAT32) para organizar y almacenar datos.
  </div>
</details>

<details class="quiz-option incorrect">
  <summary>C) Una copia de seguridad.</summary>
  <div class="feedback">
    <div class="feedback-title">✗ Incorrecto</div>
    Aunque se pueda destinar una partición secundaria a almacenar respaldos, particionar el mismo disco físico no protege frente a un fallo mecánico o electrónico de la unidad.
  </div>
</details>

<details class="quiz-option incorrect">
  <summary>D) Un programa antivirus.</summary>
  <div class="feedback">
    <div class="feedback-title">✗ Incorrecto</div>
    No es una aplicación de seguridad, sino una estructura lógica del almacenamiento.
  </div>
</details>

---

### Pregunta 5
¿Cuál de estos dispositivos permite arrancar un equipo?

<details class="quiz-option correct">
  <summary>A) USB.</summary>
  <div class="feedback">
    <div class="feedback-title">✓ ¡Exacto!</div>
    Las memorias flash <strong>USB</strong> preparadas como medios booteables (mediante herramientas como Rufus, Ventoy o BalenaEtcher) son reconocidas por el firmware BIOS/UEFI como dispositivos de arranque externos para instalar sistemas operativos o ejecutar entornos de diagnóstico (<em>Live USB</em>).
  </div>
</details>

<details class="quiz-option incorrect">
  <summary>B) Monitor.</summary>
  <div class="feedback">
    <div class="feedback-title">✗ Incorrecto</div>
    Es un periférico exclusivo de salida visual; no almacena código de arranque.
  </div>
</details>

<details class="quiz-option incorrect">
  <summary>C) Teclado.</summary>
  <div class="feedback">
    <div class="feedback-title">✗ Incorrecto</div>
    Es un periférico de entrada HID; únicamente permite interactuar con el menú de arranque o el setup de la BIOS/UEFI.
  </div>
</details>

<details class="quiz-option incorrect">
  <summary>D) Altavoz.</summary>
  <div class="feedback">
    <div class="feedback-title">✗ Incorrecto</div>
    Es un periférico de salida de audio sin capacidad de almacenamiento ni arranque.
  </div>
</details>
