# PROPUESTA PROYECTO ASIR  Carlos Castillo Gonzalez
**Módulo** “Proyecto de Administración de Sistemas Informáticos en Red”  
**Alumno:Carlos Castillo Gonzalez**  
**Fecha:**  
________________________________________

## Índice

1. Título y descripción general del proyecto    
2. Identificación del proyecto  
3. Justificación y objetivos    
4. Contenidos y aspectos principales   
5. Medios que se utilizarán    
6. Áreas del ciclo formativo   
7. ¿Qué es Ansible?   
8. ¿Qué es Proxmox?   
9. Esquema del despliegue   

---

# 1. Título y descripción general del proyecto
![image](https://github.com/user-attachments/assets/a5c7c700-ee6d-47cd-bbb0-68efda6e42f4)

**"Automatiza tu infraestructura, simplifica tu gestión"**

**Título:** Automatización y despliegue de Infraestructura con Proxmox y Ansible.

**Descripción General:**  
Este proyecto se centra en la automatización del despliegue y gestión de infraestructura virtual utilizando Proxmox VE y Ansible. El objetivo es establecer una solución robusta y escalable que permita la creación, configuración y administración de máquinas virtuales de manera eficiente y reproducible.

---

# 2. Identificación del proyecto

- **Participantes:** Carlos Castillo González  
- **Ciclo formativo:** ASIR  
- **Centro educativo:** IES Albarregas  

---
# 2. Planteamiento del problema a resolver

Cuando tenemos que montar laboratorios o entornos de prácticas en clase, normalmente hay que crear muchas máquinas virtuales, instalarles los sistemas operativos, configurar la red, poner usuarios y dejarlo todo listo para usar. Si esto lo hacemos a mano, cada vez que un profesor o un alumno necesita un entorno nuevo, hay que repetir todos los pasos uno a uno: descargar la ISO, instalar, poner la IP, instalar programas, etc.

Esto no solo lleva **mucho tiempo** y es **aburrido**, sino que además **es fácil cometer errores**: a veces se nos olvida algún paso, otras veces no ponemos las mismas configuraciones, o si tenemos que repetir todo para otro grupo, puede que no quede igual. Si encima hay que montar muchas máquinas, la cosa se complica mucho y puede ser un lío.

Además, si alguien nuevo llega y quiere repetir la práctica, a veces no está claro qué hay que hacer o cómo lo hicimos la vez anterior, porque no está bien documentado o cada uno lo hace a su manera.

Por eso, el **problema principal** es que hacer todo esto de forma manual es lento, poco fiable y difícil de repetir siempre igual. Esto hace que sea complicado montar laboratorios grandes, corregir errores o simplemente ahorrar tiempo para dedicarlo a otras tareas más útiles.

La solución que planteo es automatizarlo todo, para que con unos pocos comandos se puedan crear y configurar todas las máquinas de manera rápida, igual para todos y sin errores, haciendo el trabajo mucho más fácil para profesores y alumnos.

---
# 3. Justificación y objetivos

### Justificación del Proyecto:

Hoy en día, la gestión de la infraestructura de TI enfrenta muchos desafíos, especialmente en lo que tiene que ver con la escalabilidad, la eficiencia y la capacidad de repetir procesos de manera confiable. Para solucionar estos problemas, es muy importante automatizar ciertas tareas, ya que esto ayuda a reducir los errores humanos, agilizar los tiempos de implementación y garantizar que los entornos de desarrollo y producción sean consistentes.

Con este proyecto, se pretende abordar estos desafíos mediante el uso de Proxmox VE para la virtualización y Ansible para la automatización, logrando así una gestión más eficiente y optimizada de los recursos tecnológicos.

### Objetivos que se Pretenden Conseguir:

1. Implementar una plataforma de virtualización utilizando Proxmox VE.  
2. Automatizar el despliegue y configuración de máquinas virtuales con Ansible. Este proyecto está diseñado para un entorno el cual será utilizado por mis compañeros David, Daniel, Víctor y Jesús.  
3. Establecer una arquitectura de desarrollo eficiente y escalable.  
4. Reducir tiempos de despliegue y minimizar errores humanos.  
5. Documentar el proceso y las mejores prácticas para futuros proyectos.

---

# 4. Contenidos y aspectos principales

### Funcionalidad que se Implementará:

- **Instalación de Ansible en el Servidor Físico:** Configuración del servidor físico para ejecutar Ansible.  
- **Despliegue de Proxmox VE:** Instalación y configuración de Proxmox VE.  
- **Automatización con Ansible:** Creación de playbooks de Ansible para automatizar el despliegue y configuración de máquinas virtuales en Proxmox.  
- **Gestión de Máquinas Virtuales:** Configuración de almacenamiento y redes, creación de plantillas de VMs, y despliegue de varias VMs con diferentes configuraciones.  

### Cómo se va a Implementar:

**Instalación de Ansible en el Servidor Físico:**

- Instalar Ansible en el servidor físico desde el cual se gestionará toda la infraestructura.  
- Configurar el entorno de Ansible y preparar los playbooks necesarios.

**Despliegue de Proxmox VE:**

- Descargar e instalar Proxmox VE en el servidor físico.  
- Configurar el almacenamiento y las redes necesarias.  
- Crear plantillas de VMs para agilizar futuros despliegues.

**Creación de Playbooks de Ansible:**

- Desarrollar playbooks para instalar Proxmox VE.  
- Crear playbooks para desplegar y configurar VMs en Proxmox.  
- Automatizar tareas de mantenimiento y monitorización.

**Despliegue y Configuración de VMs:**

- Utilizar los playbooks de Ansible para desplegar VMs con diferentes configuraciones.  
- Configurar la red y el almacenamiento de las VMs.  
- Implementar scripts de post-despliegue para la configuración adicional de las VMs.

---

# 5. Medios que se utilizarán

### Arquitectura de Desarrollo:

- **Sistema Operativo del Servidor:** Proxmox VE basado en Debian.  
- **Lenguaje de Servidor:** Bash para scripts de configuración y Ansible para la automatización.  
- **Lenguaje de Cliente:** No aplica directamente, pero se podrían utilizar herramientas de administración web para Proxmox.  
- **Framework:** Ansible para la automatización.  
- **Sistema de Gestión de Bases de Datos (SGBD):** No se requiere un SGBD específico para la configuración inicial, aunque se puede utilizar MySQL o PostgreSQL para aplicaciones específicas dentro de las VMs.  
- **Herramientas de Monitorización:** Se podrían utilizar herramientas como Prometheus y Grafana para supervisar el estado de las VMs y el servidor Proxmox.  
- **Control de Versiones:** Git para el versionado de los playbooks de Ansible y scripts de configuración.

---

# Comparativa: Proxmox + Ansible vs. Vagrant

### ¿Qué es Vagrant?
[Vagrant](https://www.vagrantup.com/) es una herramienta de automatización de entornos de desarrollo que permite crear y gestionar máquinas virtuales de forma sencilla, principalmente sobre hipervisores locales como VirtualBox, VMware, Hyper-V o incluso sobre proveedores cloud. Se utiliza mucho para laboratorios, testing y desarrollo de software, ya que facilita la creación de entornos reproducibles con simples archivos de configuración llamados `Vagrantfile`.

---

### Tabla comparativa

| Característica           | Proxmox + Ansible                               | Vagrant                        |
|--------------------------|------------------------------------------------|-------------------------------|
| **Enfoque**              | Administración, automatización y orquestación de infraestructuras reales y de laboratorio, con gestión de redes, almacenamiento, clúster, alta disponibilidad, etc. | Automatización de entornos de desarrollo y pruebas, principalmente orientado a la creación rápida de VMs locales para desarrolladores. |
| **Hipervisor**           | Proxmox (KVM y LXC, orientado a servidores)    | VirtualBox, VMware, Hyper-V, Docker (orientado a escritorio/desarrollo) |
| **Escalabilidad**        | Muy alta: soporta clúster, HA, redes avanzadas, almacenamiento centralizado, cientos de VMs y contenedores. | Limitada al entorno local o a lo que soporte el hipervisor subyacente. |
| **Automatización**       | Ansible permite automatizar desde la provisión hasta la configuración avanzada, integración con monitorización, backups, etc. | Automatización básica de aprovisionamiento y configuración inicial con shell scripts, Ansible, Puppet, Chef, etc. |
| **Producción**           | Es un stack utilizado en entornos reales y empresariales, tanto para laboratorios como para producción. | Muy orientado a desarrollo, no a sistemas en producción. |
| **Integración con otras herramientas** | Muy buena: Ansible es estándar en automatización, Proxmox tiene API y soporte para herramientas de backup, monitorización, etc. | Puede integrarse con herramientas de configuración, pero el ciclo de vida está enfocado a la VM local. |
| **Gestión de red y almacenamiento** | Completa: bridges, VLANs, almacenamiento compartido, snapshots, etc. | Limitada, depende del hipervisor (VirtualBox, etc.). |
| **Interfaz de usuario**  | Web, CLI y API REST (Proxmox), CLI y YAML (Ansible) | CLI (vagrant), algunos plugins GUI pero limitada |
| **Reproducibilidad**     | Muy alta, infraestructuras complejas replicables y versionables (IaC). | Muy buena para entornos simples de desarrollo. |

---

### ¿Por qué Proxmox + Ansible es más adecuado en este TFG?

- **Enfoque profesional y educativo:** Proxmox + Ansible permite trabajar con una infraestructura más parecida a la que se encuentra en empresas (clúster, alta disponibilidad, redes avanzadas, gestión de usuarios, snapshots, backups centralizados, etc.), mientras que Vagrant está pensado para laboratorios de desarrollo locales.
- **Escalabilidad y flexibilidad:** Proxmox puede manejar decenas o cientos de VMs y contenedores, con almacenamiento y redes avanzadas, lo que resulta idóneo para simular escenarios complejos o reales en el aula o laboratorio.
- **Automatización real de ciclo de vida:** Ansible no solo despliega, sino que configura, actualiza, monitoriza y mantiene los sistemas, y puede integrarse con pipelines CI/CD, monitorización y backup. Vagrant automatiza principalmente la creación y destrucción de VMs, no su gestión avanzada.
- **Reproducibilidad y estandarización:** La infraestructura definida en Proxmox y gestionada por Ansible es completamente replicable y versionable (IaC), lo que facilita la colaboración y la documentación en el entorno educativo.
- **Preparación para el mundo real:** Aprender Proxmox y Ansible es más útil como base profesional, ya que son herramientas ampliamente usadas en empresas, centros de datos y plataformas de cloud privado, mientras que Vagrant es más habitual entre desarrolladores de software que necesitan entornos efímeros.

---

### ¿Cuándo elegir Vagrant?

- Si el objetivo es crear rápidamente entornos de desarrollo para pruebas de software, sin necesidad de alta disponibilidad, redes avanzadas o gestión a nivel de infraestructura.
- Si se busca simplicidad máxima y el entorno de laboratorio se puede limitar a una sola máquina.
- Si los recursos hardware son muy limitados y solo se dispone de una máquina local para hacer pruebas.

---

**En resumen:**  
Proxmox + Ansible es la solución más adecuada para un TFG de administración de sistemas porque permite cubrir todo el ciclo de vida de la infraestructura, automatizar tareas avanzadas y simular entornos reales y empresariales, mientras que Vagrant está más enfocado a laboratorios de desarrollo individuales y entornos sencillos.

# 6. Áreas del ciclo formativo

- Implantación  
- Administración de sistemas  
- Redes  

---
# Contextualización de herramientas

## 7. ¿Qué es Ansible?

Ansible es una herramienta que permite automatizar la gestión de servidores sin necesidad de instalar programas adicionales en ellos. Usa archivos en formato YAML llamados playbooks para definir qué tareas deben ejecutarse en cada servidor.

### Componentes principales:

- **Nodo de Control:** Es el servidor donde se instala Ansible y desde donde se envían los comandos a los demás dispositivos.  
- **Nodos Gestionados:** Son los servidores que Ansible administra y a los que se conecta mediante SSH o WinRM.  
- **Playbooks:** Son listas de tareas escritas en YAML que indican qué acciones deben ejecutarse en los servidores.  
- **Inventario:** Es un archivo que agrupa los servidores para que puedan ser gestionados de manera organizada.

### Funcionamiento:

Ansible sigue un modelo en el que el nodo de control envía los comandos a los servidores y ejecuta tareas como instalar programas o modificar configuraciones. Además, usa un principio llamado *idempotencia*, lo que significa que, si ejecutas un playbook varias veces, el resultado será siempre el mismo sin causar cambios innecesarios.

### Relación con Python:

Ansible está desarrollado en Python y usa este lenguaje para ejecutar sus tareas. También permite a los usuarios crear módulos personalizados en Python para ampliar sus funciones.

**En resumen**, Ansible es una herramienta útil para automatizar procesos en servidores de manera sencilla y eficiente.

---

## 8. ¿Qué es Proxmox?

**Proxmox Virtual Environment (Proxmox VE)** es una plataforma de virtualización de código abierto basada en Debian que permite administrar máquinas virtuales y contenedores de manera sencilla. Usa KVM para la virtualización completa y LXC para contenedores ligeros.

### Características principales:

- **Virtualización completa y ligera:** Permite ejecutar máquinas virtuales con KVM y contenedores con LXC.  
- **Gestión centralizada:** Cuenta con una interfaz web fácil de usar para administrar servidores y recursos.  
- **Alta disponibilidad:** En un clúster, las máquinas virtuales pueden moverse automáticamente en caso de fallos.  
- **Almacenamiento flexible:** Compatible con distintos tipos de almacenamiento.  
- **Respaldo y recuperación:** Permite realizar copias de seguridad para proteger los datos.

### Ventajas de Proxmox VE:

- Código abierto, lo que permite modificar y mejorar su funcionamiento.  
- Comunidad activa que ofrece soporte y documentación.  
- Integración con Ansible y otras herramientas para automatizar la gestión de servidores.

**En conclusión**, Ansible y Proxmox VE juntos son una gran opción para automatizar y gestionar la infraestructura de TI, permitiendo a los administradores enfocarse en tareas más importantes.

---

# 9. Esquema del despliegue

*![image](https://github.com/user-attachments/assets/a950c848-e72c-4f0e-a3fb-364b3f08e394)*

---

# 10. Desarrollo

### 1. Instalación de máquina Ansible:

Lo primero que haremos será instalar el controlador de todo, el servidor Ansible. Para ello, lo que haremos será instalar un Ubuntu Server. Una vez instalado, he agregado una red anfitrión para poder trabajar mediante Termius, ya que el trabajar con un Ubuntu Server se hace bastante tedioso. También he agregado una red interna, cuya IP es una `192.168.100.2`, la cual utilizaré para comunicar las máquinas localmente. Una vez agregadas, debemos configurar el **netplan** de la máquina y agregarlas a este archivo.

---

### 2. Instalaciones necesarias en Ansible:

Para poder comenzar a preparar el despliegue hacia Proxmox mediante Ansible, debemos instalar una serie de dependencias. Lo primero será realizar el típico:

```bash
sudo apt update && sudo apt upgrade -y
```

A continuación, instalaremos Python (es necesario para ejecutar Ansible) y pip (el gestor de paquetes de Python):

```bash
sudo apt install -y python3 python3-pip
```

Tras esto, debemos instalar Ansible. En mi caso, haré uso del repositorio oficial de Ansible:

```bash
sudo apt install -y software-properties-common
sudo add-apt-repository --yes --update ppa:ansible/ansible
sudo apt install -y ansible
```

Verificamos instalación:

```bash
ansible --version
```

*![image](https://github.com/user-attachments/assets/c42078e8-1a9f-4255-90b8-232bce4c8cad)*


Ahora, instalaremos las dependencias necesarias para que Ansible interactúe con Proxmox:

```bash
ansible-galaxy collection install community.general
```

Instalamos también `proxmoxer` y `requests` haciendo uso de pip, pero primero, instalamos `venv`, el cual nos proporcionará un entorno virtual para Python:

Lo instalaremos mediante paquetes de Ubuntu:

```bash
sudo apt install -y python3-requests python3-proxmoxer
```

Aquí tendríamos nuestra máquina Ansible, en la cual realizaremos diferentes playbooks e inventarios para gestionar el despliegue.

*![image](https://github.com/user-attachments/assets/252faf9c-2cc8-406e-ae94-23d30b9883f5)*

---

### 3. Instalación de Proxmox:

Descargaremos la ISO de Proxmox desde su página oficial y crearemos una máquina virtual tal que así:

*![image](https://github.com/user-attachments/assets/7e4ecee8-2be2-4a31-8231-be7e4f3ea151)*

Una vez creada, la instalaremos. Aunque antes de instalarla, le agregaré una red interna para que se pueda conectar con la máquina Ansible. En la instalación, nos requerirá una IP la cual será la de nuestra red interna, en mi caso la `192.168.100.3`.

Una vez instalada, borramos el disco de instalación.

---

### Configuración de interfaces de red
En este caso, configuré tres interfaces de red, conectadas a tres bridges de Proxmox que representan distintas zonas de red, a las cuales se conectarán las máquinas desplegadas en proxmox:

| Interfaz | Bridge | Función | Subred          |
|----------|--------|---------|-----------------|
| net0     | vmbr0  | WAN     | 172.17.10.0/24  |
| net1     | vmbr1  | LAN     | 192.168.10.0/24 |
| net2     | vmbr2  | DMZ     | 192.168.20.0/24 |

### 4. Instalación Ubuntu Cliente:

Instalaremos un Ubuntu cliente para así poder acceder a la interfaz de Proxmox y realizar nuestras configuraciones. Una vez instalado el Ubuntu cliente y configurada la red interna, nos dirigimos a Internet y ponemos:

```
http://192.168.100.3:8006
```

*![image](https://github.com/user-attachments/assets/0cedb007-35a1-4d5d-b6a1-bdd004b9abfd)*


Una vez logueados, ya tendríamos disponible nuestra interfaz de Proxmox, la cual trataremos de utilizar lo menos posible ya que con Ansible, podremos gestionar la mayoría de las operaciones a realizar para el despliegue, aunque sí tendremos que usarla para algunas configuraciones.

---

# Varios tipos de despliegue

## Despliegue desde imagen cloud-init

### 1. Creación de carpeta de trabajo:

Una vez ya instalado y configurado Proxmox, ya podemos comenzar con la preparación del despliegue de la primera máquina. Para ello, nos dirigimos a la máquina Ansible y creamos una carpeta para el trabajo:

*![image](https://github.com/user-attachments/assets/a45e3b75-8a5f-4496-baf7-968b8dcccff4)*

Una vez creada la carpeta, organizaremos los archivos necesarios en 3 partes:

- **Inventario**
- **Playbooks**
- **Cloud-init**

*![image](https://github.com/user-attachments/assets/ed84593a-228f-484d-be81-93404573ed17)*

### 2. Creación de Inventario:

Comenzaremos a crear nuestro inventario. Un inventario en Ansible es simplemente un archivo o una lista que contiene los detalles de los servidores o máquinas a los que Ansible debe conectarse para ejecutar tareas. Este archivo especifica las direcciones IP, nombres de host, o grupos de servidores que quieres gestionar, lo que permite a Ansible saber a dónde enviar las instrucciones. Es como una agenda donde se guardan los contactos (servidores) con los que vas a trabajar. Como de momento solo vamos a desplegar una máquina, este será bastante sencillito, pero se complicará más cuando el despliegue sea más completo.

-**Lo primero** que especificaré en el inventario será el localhost, indicando que la conexión serálocal y que haga uso de python3 para ejecutar comandos. se define tal que así: 

```bash
[local]
localhost ansible_connection=local ansible_python_interpreter=/usr/bin/python3
```
-**Lo segundo** que especificaré será la máquina proxmox, en la cual si debemos especificar la IP a la que se debe conectar para la ejecución de los comandos. Tambien espefcificaremos el usuario y la contraseña:

```bash
[proxmox]
192.168.100.3 ansible_user=root ansible_password=carlos ansible_connection=ssh ansible_python_interpreter=/usr/bin/python3
```
-**Y por últimmo (de momento)** especificaremos la máquina snort (es la que vamos a desplegar):

```bash
[snort]
snort ansible_host=192.168.100.10 ansible_user=carlos ansible_password=carlos ansible_become=true
```
-**El inventario quedaría tal que así, guardado en un archivo .ini**

*![image](https://github.com/user-attachments/assets/63410708-1d6f-45ab-bfcf-599d112bc9ff)*

### 3. Creación de Playbook:

Una vez creado el inventario, procederemos a crear el Playbook para el despliegue de la máquina. Un playbook en Ansible es un archivo donde defines una serie de tareas o acciones que quieres que Ansible ejecute en tus máquinas. Es como una receta o un conjunto de instrucciones que le dices a Ansible para automatizar tareas, como instalar programas, configurar servicios, o hacer cambios en los sistemas. Cada tarea en un playbook describe qué hacer, en qué máquinas hacerlo y cómo hacerlo.

*Este playbook despliega una máquina virtual Ubuntu en Proxmox con Cloud-Init y Snort. Básicamente:*

- Verifica si la imagen de Ubuntu ya está disponible.

- Crea una VM vacía en Proxmox con la configuración especificada (memoria, CPU, red, etc.).

- Importa la imagen de Ubuntu si no está presente.

- Adjunta el disco importado a la VM.

- Configura el arranque desde el disco.

- Deshabilita KVM en la VM (opcional, para configuración especial).

- Crea una unidad Cloud-Init para configurar la VM.

- Genera los archivos de configuración de Cloud-Init (user-data y network-config).

- Adjunta estos archivos de configuración a la VM.

- Inicia la VM y espera que se inicie correctamente.

**Y así quedaría mi playbook el cual logra desplegar la máquina correctamente, guardado en un .yml**
```bash
 ---
- name: Desplegar VM Ubuntu Cloud-Init con Snort
  hosts: localhost
  gather_facts: false

  vars:
    vm_id: 105
    vm_name: "ubuntu-snort"
    vm_memory: 4096
    vm_cores: 2
    vm_ip: "192.168.100.10"
    vm_gateway: "192.168.100.3"
    vm_network_interface: "ens18"
    cloud_init_user: "carlos"
    cloud_init_password: "carlos"
    image_path: "/var/lib/vz/template/iso/jammy-server-cloudimg-amd64.img"
    storage: "local-lvm"
    proxmox_host: "192.168.100.3"
    proxmox_node: "carlos"
    snippets_path: "/var/lib/vz/snippets"

  tasks:

    - name: Verificar si la imagen cloud existe
      stat:
        path: "{{ image_path }}"
      register: image_stat

    - name: Crear la VM vacía
      community.general.proxmox_kvm:
        api_host: "{{ proxmox_host }}"
        api_user: "root@pam"
        api_password: "carlos"
        vmid: "{{ vm_id }}"
        node: "{{ proxmox_node }}"
        name: "{{ vm_name }}"
        memory: "{{ vm_memory }}"
        cores: "{{ vm_cores }}"
        ostype: l26
        scsihw: virtio-scsi-pci
        net:
          net0: "virtio,bridge=vmbr0"
        ipconfig:
          ipconfig0: "ip={{ vm_ip }}/24,gw={{ vm_gateway }}"
        state: present
      delegate_to: localhost

    - name: Importar el disco a la VM
      command: qm importdisk {{ vm_id }} {{ image_path }} {{ storage }}
      when: not image_stat.stat.exists
      delegate_to: "{{ proxmox_host }}"

    - name: Adjuntar disco importado como scsi0
      command: qm set {{ vm_id }} --scsihw virtio-scsi-pci --scsi0 {{ storage }}:vm-{{ vm_id }}-disk-0
      delegate_to: "{{ proxmox_host }}"

    - name: Configurar arranque desde el disco
      command: qm set {{ vm_id }} --boot order=scsi0
      delegate_to: "{{ proxmox_host }}"

    - name: Deshabilitar KVM en la VM
      command: qm set {{ vm_id }} --kvm 0
      delegate_to: "{{ proxmox_host }}"
      changed_when: false

    - name: Crear unidad Cloud-Init
      command: qm set {{ vm_id }} --ide2 {{ storage }}:cloudinit,media=cdrom
      delegate_to: "{{ proxmox_host }}"

    - name: Generar user-data
      template:
        src: ../cloud_init/snort-user-data.yml.j2
        dest: "{{ snippets_path }}/{{ vm_name }}-user-data.yml"
      delegate_to: "{{ proxmox_host }}"

    - name: Generar network-config
      template:
        src: ../cloud_init/snort-network-config.yml.j2
        dest: "{{ snippets_path }}/{{ vm_name }}-network-config.yml"
      delegate_to: "{{ proxmox_host }}"

    - name: Adjuntar configuración Cloud-Init personalizada
      command: >
        qm set {{ vm_id }} --cicustom "user=local:snippets/{{ vm_name }}-user-data.yml,network=local:snippets/{{ vm_name }}-network-config.yml"
      delegate_to: "{{ proxmox_host }}"

    - name: Iniciar la VM
      community.general.proxmox_kvm:
        api_host: "{{ proxmox_host }}"
        api_user: "root@pam"
        api_password: "carlos"
        vmid: "{{ vm_id }}"
        node: "{{ proxmox_node }}"
        state: started
        timeout: 300
      delegate_to: localhost
```
### 4. Configuración Cloud-Init:

Debemos crear y configurar una carpeta cloud-init para la máquina. ¿Por qué? Configurar Cloud-Init en esta máquina virtual es necesario porque Cloud-Init permite automatizar la configuración inicial del sistema operativo cuando la máquina se inicia por primera vez. En este caso, la configuración de Cloud-Init hace lo siguiente:

- Crea el usuario especificado (en este caso, "carlos") y configura su contraseña automáticamente.

- Configura la red de la máquina, asegurando que tenga una dirección IP estática y la puerta de enlace correcta.

- Realiza configuraciones adicionales como la instalación de paquetes o ajustes específicos del sistema, que son definidos en los archivos user-data y network-config.

Para ello, crearemos 2 archivos, uno configurará la información del usuario de la máquina y el otro configurará la red de la misma:
- **snort-user-data.yml.j2**
```bash
#cloud-config
hostname: {{ vm_name }}
users:
  - name: {{ cloud_init_user }}
    sudo: ALL=(ALL) NOPASSWD:ALL
    groups: sudo
    home: /home/{{ cloud_init_user }}
    shell: /bin/bash
    lock_passwd: false
    passwd: "{{ cloud_init_password | password_hash('sha512') }}"
ssh_pwauth: true
disable_root: false
chpasswd:
  expire: false

package_update: true
packages:
  - snort

bootcmd:
  - echo 'ttyS0' > /etc/securetty

runcmd:
  - netplan apply
  - systemctl enable snort
```

- **snort-network-config.yml.j2**
```bash
#cloud-config
hostname: {{ vm_name }}
users:
  - name: {{ cloud_init_user }}
    sudo: ALL=(ALL) NOPASSWD:ALL
    groups: sudo
    home: /home/{{ cloud_init_user }}
    shell: /bin/bash
    lock_passwd: false
    passwd: "{{ cloud_init_password | password_hash('sha512') }}"
ssh_pwauth: true
disable_root: false
chpasswd:
  expire: false

package_update: true
packages:
  - snort

bootcmd:
  - echo 'ttyS0' > /etc/securetty

runcmd:
  - netplan apply
  - systemctl enable snort

carlos@ansible:~/proyecto2/cloud_init$ cat snort-network-config.yml.j2
version: 2
ethernets:
  {{ vm_network_interface }}:
    dhcp4: false
    addresses:
      - {{ vm_ip }}/24
    gateway4: {{ vm_gateway }}
    nameservers:
      addresses: [8.8.8.8, 1.1.1.1]
```
### 5. Subir imagen a proxmox:

Antes de ejecutar el playbook, debemos subir la imagen que tendrá la máquina que desplegaremos. Esto lo haremos mediante la interfaz gráfica.

Para ello, nos direigimos a la interfaz proxmox, seleccionamos el nodo, seleccionamos el almacenamiento, vamos a ISOS y cargamos la imagen previamente descargada:

*![image](https://github.com/user-attachments/assets/c09288f3-0802-4f33-a65b-fd31d417c981)*

### 6. Ejecutar playbook y confirmar despliegue:

Una vez preparados todos los archivos y la imagen, tendríamos todo listo para ejecutar el playbook y conseguir el despliegue de la primera máquina. Para ello, ejecutamos el comando siguiente:
```bash
ansible-playbook -i inventory.ini playbooks/snort.yml
```
Con este comando, ejecutaremos el playbook que orquesta el despliegue como root. Se vería tal que así:

*![image](https://github.com/user-attachments/assets/fff6effc-55e5-4fd3-b3ed-0437bea92311)*

*![image](https://github.com/user-attachments/assets/1c2d976e-df59-4716-ac5e-f1358d3ec7e9)*

**Como se indica, todo está correcto (changed indica que se han aplicado cambios)**

### 7. Confirmación de la máquina:

Una vez terminado el despliegue, nos dirigiremos a la interfaz Proxmox para comprobar que todo ha sido creado correctamente:
- **Su configuración hardware**
  
 *![image](https://github.com/user-attachments/assets/9445eba3-eec3-4592-a47d-42cb9934b0e5)*

- **Consola de la máquina**
  
 *![image](https://github.com/user-attachments/assets/b2517beb-1b7f-43df-aff6-44746f557d62)*

- **Su IP y conectividad con Proxmox**
  
  *![image](https://github.com/user-attachments/assets/8f9eccab-bcd2-4f48-9c19-69f0a726362a)*
  
  *![image](https://github.com/user-attachments/assets/421b1891-0a95-4d82-a400-42b0548d226b)*

- **Comprobar si Snort está instalado**
  
  *![image](https://github.com/user-attachments/assets/0c7cd2ed-6745-4c6f-a768-c8cad462f80c)*

## 10. Despliegue de máquina OVA:

Una opción muy buena de proxmox y que nos ahorraría aún más tiempo, sería instalr una OVA con todo lo necesario para nuestro entorno de trabajo ya instaldo. Para ello, crearemos un playbook con los requerimientos necesarios:
  
###  Descripción del Playbook

Este playbook permite automatizar todo el ciclo de vida de una VM a partir de una OVA:

- Extrae y convierte la imagen OVA.
- Crea una VM vacía con la configuración deseada.
- Importa y conecta el disco a la VM.
- Establece opciones de arranque y salida gráfica.
- Inicia la VM para que comience a ejecutarse.
  
**Y así quedaría mi playbook el cual logra desplegar la máquina correctamente:
```bash
- name: Convertir misma OVA y desplegar segunda VM con 3 interfaces de red
  hosts: pve
  become: true
  gather_facts: false

  vars:
    vm_id: 106  # ID distinto a la primera VM
    vm_name: "ubuntu-snort-2"  # Nombre distinto
    vm_memory: 4096
    vm_cores: 2
    storage: "local-lvm"
    bridge: "vmbr0"
    ova_path: "/var/lib/vz/template/iso/Snort_2.ova"  # MISMA OVA
    extracted_dir: "/var/lib/vz/template/iso/snort2-vm2"  # Carpeta distinta
    qcow2_path: "/var/lib/vz/template/iso/snort2-vm2/ubuntu-snort-2.qcow2"  # Disco diferente

  tasks:

    - name: Crear carpeta para extraer OVA
      file:
        path: "{{ extracted_dir }}"
        state: directory
        mode: '0755'

    - name: Extraer OVA
      unarchive:
        src: "{{ ova_path }}"
        dest: "{{ extracted_dir }}"
        remote_src: yes

    - name: Buscar archivo VMDK
      find:
        paths: "{{ extracted_dir }}"
        patterns: "*.vmdk"
        recurse: no
      register: vmdk_files

    - name: Eliminar archivo existente disk.vmdk si ya existe
      file:
        path: "{{ extracted_dir }}/disk.vmdk"
        state: absent

    - name: Renombrar archivo VMDK a disk.vmdk
      command: mv "{{ item.path }}" "{{ extracted_dir }}/disk.vmdk"
      loop: "{{ vmdk_files.files }}"
      loop_control:
        loop_var: item
      when: item.path != "{{ extracted_dir }}/disk.vmdk"

    - name: Convertir VMDK a QCOW2
      command: qemu-img convert -f vmdk -O qcow2 {{ extracted_dir }}/disk.vmdk {{ qcow2_path }}

    - name: Crear VM vacía
      command: >
        qm create {{ vm_id }}
        --name {{ vm_name }}
        --memory {{ vm_memory }}
        --cores {{ vm_cores }}

    - name: Importar disco QCOW2
      command: qm importdisk {{ vm_id }} {{ qcow2_path }} {{ storage }}

    - name: Adjuntar disco como scsi0
      command: qm set {{ vm_id }} --scsihw virtio-scsi-pci --scsi0 {{ storage }}:vm-{{ vm_id }}-disk-0

    - name: Establecer disco de arranque
      command: qm set {{ vm_id }} --boot order=scsi0

    - name: Configurar salida gráfica estándar en la VM
      command: qm set {{ vm_id }} --vga std --serial0 socket

    - name: Añadir primera interfaz de red (net0)
      command: qm set {{ vm_id }} --net0 virtio,bridge={{ bridge }}

    - name: Añadir segunda interfaz de red (net1)
      command: qm set {{ vm_id }} --net1 virtio,bridge={{ bridge }}

    - name: Añadir tercera interfaz de red (net2)
      command: qm set {{ vm_id }} --net2 virtio,bridge={{ bridge }}

    - name: Iniciar la VM
      command: qm start {{ vm_id }}
```
###  Comprobar la OVA:

Una vez creado el playbook, nos quedaría desplegarlo y comprobar que se ejecuta correctamente. Una vez se ejecute, comprobamos que se ha desplegado sin problemas:
![image](https://github.com/user-attachments/assets/d5dede77-811c-4d8f-912d-300c1f949d23)

**Cabe recalcar que todas las configuraciones deben venir previamente configuradas en la OVA, como por ejemplo, las redes o las reglas del Snort.

## 10. Despliegue de máquina OVA desde un QCOW2 directamente:

Hay veces que nos encontraremos con el disco QCOW2 directamente para poder desplegarlo, sin tener que extraer carpetas ni convertir de un formato a otro.
En esta sección explico cómo realicé el despliegue de una máquina virtual directamente desde un archivo en formato QCOW2 utilizando Ansible en un entorno Proxmox. Este método me resultó especialmente útil cuando trabajé con imágenes preconfiguradas como Kali Linux o Snort, que ya tenía en formato .qcow2, evitando así pasos adicionales de conversión desde OVA o VMDK.

### Requisitos previos

Para llevar a cabo este procedimiento, me aseguré de cumplir los siguientes requisitos:

 -Tener el archivo .qcow2 copiado en el nodo Proxmox, concretamente en la ruta:

```
/var/lib/vz/template/iso/
```

 -Configurar la conectividad SSH entre mi máquina de control (donde ejecuto Ansible) y el nodo Proxmox.

 -Tener Ansible instalado y correctamente autenticado con Proxmox.

### Subida del QCOW2 al nodo
Para subir la imagen QCOW2 al nodo, utilicé scp:

```
scp kali.qcow2 root@172.17.10.53:/var/lib/vz/template/iso/
```
### Playbook de Ansible para el despliegue
```
---
- name: Desplegar VM KALI con 3 interfaces de red
  hosts: pve
  become: true
  gather_facts: false

  vars:
    vm_id: 105
    vm_name: "kali"
    vm_memory: 4096
    vm_cores: 2
    storage: "local-lvm"
    bridge_wan: "vmbr0"
    bridge_lan: "vmbr1"
    bridge_dmz: "vmbr2"
    qcow2_path: "/var/lib/vz/template/iso/kali-linux-2025.1c-qemu-amd64.qcow2"

  tasks:

    - name: Crear VM vacía
      command: >
        qm create {{ vm_id }}
        --name {{ vm_name }}
        --memory {{ vm_memory }}
        --cores {{ vm_cores }}

    - name: Importar disco QCOW2
      command: qm importdisk {{ vm_id }} {{ qcow2_path }} {{ storage }}

    - name: Adjuntar disco como scsi0
      command: qm set {{ vm_id }} --scsihw virtio-scsi-pci --scsi0 {{ storage }}:vm-{{ vm_id }}-disk-0

    - name: Establecer disco de arranque
      command: qm set {{ vm_id }} --boot order=scsi0

    - name: Configurar salida gráfica estándar en la VM
      command: qm set {{ vm_id }} --vga std --serial0 socket

    - name: Añadir interfaz de red WAN (net0)
      command: qm set {{ vm_id }} --net0 virtio,bridge={{ bridge_wan }}

    - name: Añadir interfaz de red LAN (net1)
      command: qm set {{ vm_id }} --net1 virtio,bridge={{ bridge_lan }}

    - name: Añadir interfaz de red DMZ (net2)
      command: qm set {{ vm_id }} --net2 virtio,bridge={{ bridge_dmz }}

    - name: Iniciar la VM
      command: qm start {{ vm_id }}
```

### Comprobamos el despliegue

![image](https://github.com/user-attachments/assets/d31307d9-2229-4584-ab1d-337a88c45130)


![image](https://github.com/user-attachments/assets/743d95c1-e33b-4e70-8c77-0e98d0626f8d)

## Clonado de una Máquina Virtual desde Plantilla en Proxmox

Una vez creada la plantilla base (por ejemplo, desde una OVA previamente importada y personalizada), es posible clonar dicha plantilla para desplegar nuevas máquinas virtuales de forma rápida y consistente.

### 1. Verificar Plantillas Disponibles

Primero, se puede listar el estado actual de las máquinas virtuales y plantillas con el siguiente comando:

```bash
qm list
```

Las plantillas aparecerán indicadas como `template` en la columna correspondiente.

### 2. Clonar la Plantilla

Se utiliza el siguiente comando para clonar la plantilla. Este proceso genera una nueva máquina virtual completamente funcional a partir de la plantilla:

```bash
qm clone <ID_plantilla> <ID_nueva_vm> --name <nombre_nuevo>
```

**Ejemplo práctico:**

```bash
qm clone 105 108 --name kali
```

Esto crea una nueva máquina virtual con ID `108` y nombre `kali` a partir de la plantilla con ID `105`.


### 3. Configuración de las Interfaces de Red

Después del clonado, se pueden configurar las interfaces de red necesarias en la nueva VM:

```bash
qm set 108 --net0 virtio,bridge=vmbr1
qm set 108 --net1 virtio,bridge=vmbr2
qm set 108 --net2 virtio,bridge=vmbr3
```

### 4. Iniciar la Máquina Virtual Clonada

Por último, se inicia la nueva máquina virtual con:

```bash
qm start 108
```

---

De esta manera, es posible generar múltiples entornos replicables a partir de una imagen base, optimizando el tiempo de despliegue y manteniendo coherencia en los entornos de laboratorio.

Como podemos observar, aquí tenemos la máquina que usaremos como plantilla y seguidamente los clones que hemos realizado con ella:

![Captura de pantalla 2025-06-03 140051](https://github.com/user-attachments/assets/726eaa3e-f5c5-4312-b7e4-d9702cc01d58)

![Captura de pantalla 2025-06-03 140457](https://github.com/user-attachments/assets/6e3ed693-17e7-4567-85c7-ecaa28e6a9da)

# Aplicación a entorno real

El presente proyecto ha sido diseñado y desplegado como una simulación realista de un entorno empresarial segmentado en distintas zonas de red, aplicando principios de seguridad perimetral y defensa en profundidad. Para ello, se ha empleado una infraestructura virtual basada en Proxmox VE como hipervisor y Ansible como herramienta de automatización.

## Infraestructura Virtual
La topología del entorno está estructurada en tres segmentos principales de red:

WAN (vmbr0): representa la conexión hacia el exterior.

LAN (vmbr1): red interna donde residen los sistemas internos de la organización.

DMZ (vmbr2): red perimetral expuesta donde se ubican servicios públicos como un servidor web.

Cada uno de estos segmentos ha sido implementado mediante bridges (vmbrX) en Proxmox, y cada máquina virtual ha sido conectada de forma adecuada a uno o más de estos segmentos según su rol.

### Funcionalidad de las Máquinas
 - pfSense: funciona como cortafuegos y gateway entre las distintas redes. Se conecta a las tres interfaces (WAN, LAN, DMZ) y gestiona todo el enrutamiento y las reglas de filtrado. Además, ofrece servicios de DHCP para las subredes internas.

 - Snort: IDS/IPS conectado a la red LAN, monitoriza el tráfico interno y permite detectar posibles intrusiones dentro de la organización.

 - Suricata: sistema de detección conectado a dos interfaces: una en WAN y otra en una red "WAN monitor" paralela, para realizar inspección del tráfico entrante y detectar anomalías desde el exterior sin interrumpir el tráfico directo hacia pfSense.

 - Servidor Web (DMZ): alojado en la red perimetral DMZ, expone servicios que pueden ser accedidos desde el exterior. Está aislado del resto de la infraestructura, minimizando riesgos en caso de compromiso.

 - Kali Linux: máquina atacante conectada a LAN y DMZ, utilizada en entornos de prueba para simular ataques internos y externos controlados.

 - Pila ELK (Elasticsearch, Logstash, Kibana): desplegada en LAN. Centraliza y visualiza logs provenientes de Snort, Suricata y pfSense para facilitar el análisis forense y la respuesta ante incidentes.

### Automatización del Despliegue
Todo el entorno ha sido desplegado de forma automatizada mediante Ansible, aprovechando su capacidad para interactuar con Proxmox vía API REST. El proceso incluye:

  - Conversión y despliegue de imágenes OVA/QCOW2.

  - Asignación de interfaces de red según topología.

  - Aplicación de configuraciones específicas (por ejemplo, modificación de GRUB, plantillas Cloud-Init y archivos netplan).

  - Arranque ordenado y configuración de servicios.

Gracias a esta automatización, se ha logrado replicar el entorno de forma coherente, reproducible y eficiente, facilitando futuras pruebas, análisis de seguridad y desarrollo de políticas de red.

### Aplicación Real
Este tipo de entorno es directamente aplicable a organizaciones reales que requieran segmentación de red, análisis de tráfico y simulación de ataques como parte de su estrategia de ciberseguridad. Permite emular situaciones del mundo real, validar herramientas defensivas y formar personal técnico en un entorno controlado y realista.

---

# Errores encontrados y soluciones aplicadas

Durante el desarrollo y despliegue automatizado con Ansible y Proxmox, me he encontrado con diversos errores y obstáculos técnicos. A continuación detallo algunos de los problemas reales que han surgido, cómo los he solucionado y recojo también los errores más habituales que suelen aparecer en este tipo de despliegues según la experiencia y la documentación de la comunidad.

---

### Errores reales durante mi proyecto y sus soluciones

1. **Error de autenticación SSH entre Ansible y Proxmox**
   - **Síntoma:** Al lanzar playbooks contra el nodo Proxmox, aparecía el error `Permission denied (publickey,password)`.
   - **Solución:**  
     - Verifiqué que el usuario y la contraseña en el inventario eran correctos.
     - Probé la conexión SSH manualmente (`ssh root@<IP-DEL-PROXMOX>`).
     - Tuve que copiar la clave pública SSH del servidor Ansible al nodo Proxmox con `ssh-copy-id`.
     - En algunos casos, fue necesario habilitar el acceso por contraseña en el archivo `/etc/ssh/sshd_config` y reiniciar el servicio SSH.

2. **Fallo en módulos de Ansible por dependencias de Python**
   - **Síntoma:** Errores tipo `ModuleNotFoundError: No module named 'proxmoxer'` o problemas con la colección community.general.
   - **Solución:**  
     - Instalé los módulos necesarios con `pip install proxmoxer requests`.
     - Verifiqué que el entorno virtual Python estuviera correctamente activado.
     - Instalé la colección de Ansible necesaria con `ansible-galaxy collection install community.general`.

3. **Error al importar imágenes QCOW2/OVA**
   - **Síntoma:** El comando `qm importdisk` fallaba porque la ruta del archivo era incorrecta o porque el almacenamiento seleccionado no era válido.
   - **Solución:**  
     - Revisé que la ruta de la imagen estuviera correctamente escrita y el archivo efectivamente subido al nodo.
     - Comprobé el nombre del almacenamiento en Proxmox (`local-lvm`, `local`, etc.).
     - Cambié permisos de archivos si era necesario (`chmod`).

4. **Problemas con Cloud-Init**
   - **Síntoma:** La máquina virtual desplegada no aplicaba la configuración de red o usuario definida en los archivos de Cloud-Init.
   - **Solución:**  
     - Verifiqué la sintaxis de los archivos YAML (`user-data` y `network-config`).
     - Confirmé que los archivos se copiaban correctamente en la ruta de snippets de Proxmox.
     - Aseguré que la VM tuviera el disco de Cloud-Init correctamente adjunto y que el arranque fuera desde dicho disco.

5. **Errores de permisos en Proxmox**
   - **Síntoma:** Mensajes de `permission denied` o errores al intentar crear VMs desde Ansible.
   - **Solución:**  
     - Utilicé el usuario `root@pam` para las pruebas.
     - Más adelante, creé un usuario con permisos estrictamente necesarios y le asigné los roles apropiados en Proxmox.

6. **Fallo en ejecución de playbooks por rutas relativas**
   - **Síntoma:** Ansible no encontraba archivos de plantillas o imágenes (`template not found`).
   - **Solución:**  
     - Usé rutas absolutas en los playbooks y aseguré que la estructura de carpetas fuera consistente.
     - Añadí tareas para crear directorios si no existían (`file: state=directory`).

7. **Error con la opción KVM habilitada o deshabilitada**
   - **Síntoma:** Al desplegar algunas máquinas virtuales, especialmente imágenes cloud-init o appliances importados, la VM no arrancaba correctamente o mostraba errores relacionados con la compatibilidad de hardware virtual (por ejemplo, pantallas negras, errores de arranque, o mensajes como "KVM virtualization not supported").
   - **Causa:**  
     - No todas las imágenes o sistemas operativos soportan la virtualización KVM (Kernel-based Virtual Machine) de la misma manera. Por ejemplo, algunas imágenes cloud-init o appliances pueden necesitar que KVM esté desactivado para funcionar correctamente, mientras que otras requieren que esté habilitado para aprovechar la aceleración por hardware.
   - **Solución:**  
     - Para imágenes que daban problemas, utilicé el comando:  
       ```bash
       qm set <vm_id> --kvm 0
       ```
       (esto desactiva KVM para esa VM).
     - Para sistemas que sí soportan KVM (la mayoría de sistemas Linux modernos y Windows actuales), aseguré que KVM estuviera activado con:  
       ```bash
       qm set <vm_id> --kvm 1
       ```
     - En Ansible, lo gestioné con tareas condicionales según el tipo de imagen o sistema operativo.
     - Comprobé en la documentación oficial y foros si la imagen tenía requisitos especiales sobre KVM.

---

### Errores comunes en despliegues Proxmox + Ansible y cómo prevenirlos

1. **Mal formateo del inventario de Ansible**
   - Puede provocar que las tareas no se ejecuten en los hosts correctos.  
   - **Prevención:** Validar sintaxis e IPs, y hacer pruebas con un inventario mínimo.

2. **Problemas con dependencias de Ansible/Python**
   - Si falta alguna colección o módulo, los playbooks fallarán.
   - **Prevención:** Instalar todas las dependencias y usar entornos virtuales.

3. **Errores de permisos o autenticación**
   - El acceso como root puede estar deshabilitado o mal configurado.
   - **Prevención:** Probar siempre el acceso SSH manualmente antes de automatizar.

4. **Falta de recursos físicos**
   - Si el nodo Proxmox no tiene suficiente RAM/CPU/almacenamiento, los despliegues fallan.
   - **Prevención:** Monitorizar recursos y ajustar tamaños de VM según disponibilidad.

5. **Errores en la red**
   - Una configuración incorrecta de bridges, interfaces o cloud-init puede dejar VMs sin conectividad.
   - **Prevención:** Probar la conectividad tras cada paso y documentar las configuraciones de red.

6. **Playbooks no idempotentes**
   - Si los playbooks no están bien diseñados, pueden dejar la infraestructura en un estado inconsistente.
   - **Prevención:** Usar buenas prácticas de Ansible y probar siempre con `--check`.

7. **Errores en rutas o nombres de almacenamiento en Proxmox**
   - Si se usa un nombre incorrecto, los comandos de creación de disco o importación fallan.
   - **Prevención:** Comprobar los nombres exactos en la interfaz de Proxmox antes de lanzar los playbooks.

8. **Errores con la aceleración KVM (añadido)**
   - Algunos sistemas/appliances requieren desactivar KVM, otros requieren activarlo.
   - **Prevención:** Revisar los requisitos de cada imagen, y adaptar el parámetro `--kvm` según corresponda. Probar ambos modos si aparecen errores de arranque.

---

### Recomendaciones generales para solución de problemas

- Leer cuidadosamente los logs de Ansible y Proxmox.
- Probar manualmente los comandos antes de automatizarlos.
- Comenzar con despliegues sencillos e ir añadiendo complejidad progresivamente.
- Documentar cada error y su solución para futuras referencias.
- Mantener todos los sistemas y dependencias actualizados.

---

**Conclusión:**  
Los errores forman parte natural del proceso de automatización y despliegue. La clave está en saber interpretarlos, buscar la causa raíz y documentar las soluciones, lo que a la larga ahorra tiempo y mejora la calidad de los despliegues futuros.

# 9. Conclusión

A lo largo de este proyecto he podido comprobar de primera mano la importancia de la automatización y la virtualización en la administración de sistemas modernos. Trabajar con herramientas como Proxmox y Ansible no solo me ha permitido ahorrar tiempo y esfuerzo en la creación y gestión de laboratorios virtuales, sino que también me ha ayudado a entender cómo se trabaja actualmente en empresas y centros de datos profesionales.

Gracias a este proyecto he aprendido a planificar y documentar procesos de despliegue, a resolver problemas reales que surgen en el día a día y a diseñar entornos reproducibles y escalables, algo fundamental tanto en el mundo educativo como en el profesional. Además, me ha servido para mejorar mis habilidades de troubleshooting y a valorar la importancia de dejar constancia clara de los procedimientos, para que cualquier persona pueda repetirlos o mejorarlos en el futuro.

Considero que este trabajo es muy útil para el ciclo formativo de ASIR porque acerca a los alumnos a herramientas y metodologías de uso real en la industria, fomenta el trabajo en equipo y la buena documentación, y facilita la creación de laboratorios prácticos para las asignaturas técnicas. Además, puede servir de base para futuros proyectos más ambiciosos o para la integración con otras tecnologías como la monitorización, la seguridad o el despliegue en la nube.

---

# 10. Bibliografía / recursos

- [Documentación oficial de Proxmox VE](https://pve.proxmox.com/pve-docs/)
- [Documentación oficial de Ansible](https://docs.ansible.com/)
- [Colección community.general de Ansible](https://docs.ansible.com/ansible/latest/collections/community/general/index.html)
- [Proxmoxer Python API](https://proxmoxer.readthedocs.io/en/latest/)
- [Guía Cloud-Init](https://cloudinit.readthedocs.io/en/latest/)
- [Repositorio oficial de Proxmox en GitHub](https://github.com/proxmox)
- [Repositorio oficial de Ansible en GitHub](https://github.com/ansible/ansible)
- [Manual de instalación de Proxmox VE](https://pve.proxmox.com/wiki/Install_Proxmox_VE_on_Debian_12_Bookworm)
- [QEMU/KVM Documentation](https://www.qemu.org/documentation/)
- [Tutoriales de Virtualización en YouTube](https://www.youtube.com/results?search_query=proxmox+ansible)
- [Foros oficiales de Proxmox](https://forum.proxmox.com/)
- [Foros de Stack Overflow](https://stackoverflow.com/questions/tagged/ansible+proxmox)
- [Blog de Adictos al Trabajo - Automatización con Ansible y Proxmox](https://www.adictosaltrabajo.com/2022/10/26/automatizando-proxmox-con-ansible/)
- [Linux Handbook: Ansible Playbooks](https://linuxhandbook.com/ansible-playbook-examples/)
- [Ejemplo de despliegue de VM con Cloud-Init en Proxmox](https://www.servethehome.com/using-cloud-init-images-to-deploy-ubuntu-vms-on-proxmox-ve/)

---

# 11. Glosario

- **Ansible**: Herramienta de automatización que permite gestionar la configuración, el despliegue y la orquestación de servidores desde archivos de texto (playbooks).
- **API (Application Programming Interface)**: Conjunto de funciones y protocolos que permite que programas diferentes se comuniquen entre sí y automaticen tareas.
- **Backup**: Copia de seguridad de datos o sistemas para poder restaurarlos en caso de pérdida o fallo.
- **Bridge**: Dispositivo virtual de red que simula un switch y permite conectar varias máquinas virtuales a la misma red física o virtual.
- **Cloud-Init**: Herramienta para la configuración automática de sistemas operativos la primera vez que arrancan, usando archivos de configuración.
- **Clúster**: Conjunto de servidores o nodos que trabajan juntos para aumentar la disponibilidad y/o la capacidad de procesamiento.
- **Contenedor LXC**: Tecnología de virtualización ligera incluida en Proxmox para crear contenedores Linux (similares a Docker, pero más integrados en el sistema).
- **Disco QCOW2**: Formato de disco virtual usado por QEMU/KVM, muy útil por su flexibilidad y soporte para snapshots.
- **Git**: Sistema de control de versiones distribuido que permite gestionar el historial de archivos y la colaboración en proyectos.
- **Host**: Cualquier máquina física o virtual que forma parte de una red.
- **Hypervisor**: Programa o sistema que permite ejecutar varias máquinas virtuales sobre un hardware físico.
- **Idempotencia**: Propiedad de los playbooks de Ansible por la cual, aunque se ejecuten varias veces, el resultado siempre será el mismo y no se harán cambios innecesarios.
- **Inventario**: Archivo de texto donde se listan los servidores que Ansible va a gestionar.
- **KVM**: (Kernel-based Virtual Machine) Tecnología de virtualización integrada en el kernel de Linux que permite ejecutar máquinas virtuales de alto rendimiento.
- **LVM (Logical Volume Manager)**: Sistema para gestionar particiones y volúmenes lógicos en discos duros, permitiendo mayor flexibilidad.
- **Nodo**: Cada uno de los servidores físicos o virtuales que forman parte de una infraestructura o clúster.
- **OVA (Open Virtual Appliance)**: Formato estándar para distribuir máquinas virtuales completas, que incluye la configuración y el disco duro virtual.
- **Playbook**: Archivo en formato YAML que define un conjunto de tareas automatizadas que Ansible debe ejecutar en uno o varios servidores.
- **Proxmox VE**: Plataforma de virtualización de código abierto basada en Debian, usada para crear y gestionar máquinas virtuales y contenedores.
- **Provisionar**: El proceso de preparar y configurar un sistema o servicio para su uso.
- **Repositorio**: Lugar centralizado donde se almacenan y gestionan archivos y versiones de un proyecto (por ejemplo, en GitHub).
- **Rol (Role)**: En Ansible, un conjunto de tareas, archivos y variables agrupadas para ser reutilizadas fácilmente.
- **Root**: Usuario administrador en sistemas Linux, con todos los permisos.
- **Script**: Archivo de texto que contiene una serie de comandos que se ejecutan de forma automática.
- **Snapshot**: Copia puntual del estado de una máquina virtual o sistema, útil para restaurar en caso de problemas.
- **SSH (Secure Shell)**: Protocolo seguro para conectarse y administrar servidores de forma remota.
- **Template (Plantilla)**: Máquina virtual o configuración base que se usa para crear rápidamente nuevas máquinas idénticas.
- **YAML**: Formato de texto fácil de leer y escribir, usado para definir la configuración de playbooks en Ansible y otros sistemas.
