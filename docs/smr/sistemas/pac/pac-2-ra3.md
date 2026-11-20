[← Volver al Índice de PACs](./index.md)

---

# PAC 2 (RA3) - PAC de Desarrollo: Instalación de Ubuntu 26 y Guest Additions

---

### Requisitos y Parámetros de la Práctica

* **Hipervisor:** Oracle VirtualBox
* **Sistema operativo invitado:** Ubuntu 26.04.1 LTS (*Resolute*)[cite: 2]
* **Nombre de la máquina virtual:** `Ubuntu26_LuisAlejandro_GonzalezMartinez`[cite: 2]
* **Cuenta de usuario configurada:** `luisalejandrogonzalezmartinez` (Nombre completo: `LuisAlejandro GonzalezMartinez`)[cite: 2]

---

### Pregunta 1: Instalación de Ubuntu 26

Instalación del sistema operativo libre Ubuntu 26 en una máquina virtual nueva cumpliendo con la nomenclatura requerida tanto en el hipervisor como en la cuenta de usuario local. Para verificar la distribución y versión exacta instalada, se ejecuta el comando `lsb_release -a` en la terminal[cite: 2]:

```bash
lsb_release -a
```

* **Distributor ID:** `Ubuntu`[cite: 2]
* **Description:** `Ubuntu 26.04.1 LTS`[cite: 2]
* **Release:** `26.04`[cite: 2]
* **Codename:** `resolute`[cite: 2]

<figure markdown="span" style="margin: 1.5em 0; text-align: center;">

![Instalación de Ubuntu 26 y comando lsb_release](../../img/sistemas/pac/Ub26 install Git.jpg)

<figcaption>Ventana de la máquina virtual en VirtualBox mostrando la versión de Ubuntu 26.04.1 LTS en terminal</figcaption>
</figure>

---

### Pregunta 2: Instalación de las Guest Additions

Tras completar la instalación del sistema base, se inserta la imagen ISO de las herramientas de integración de VirtualBox (*Guest Additions*) desde el menú **Dispositivos → Insertar imagen de CD de las «Guest Additions»**, se compilan e instalan los módulos del kernel necesarios y se reinicia el sistema invitado.

Una vez reiniciada la máquina virtual en modo **pantalla completa** (como solicita explícitamente el enunciado de la Pregunta 2), se comprueba el redimensionamiento dinámico de pantalla y la versión exacta de las utilidades instaladas ejecutando[cite: 3]:

```bash
VBoxControl -v
```

* **Versión instalada:** `7.2.22r175245`[cite: 3]

<figure markdown="span" style="margin: 1.5em 0; text-align: center;">

![Comprobación de Guest Additions en Ubuntu 26](../../img/sistemas/pac/Ub26 Guest.jpg)

<figcaption>Ubuntu 26.04.1 LTS en modo pantalla completa mostrando la versión de VirtualBox Guest Additions (7.2.22) en consola</figcaption>
</figure>
