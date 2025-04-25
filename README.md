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

## 1. Título y descripción general del proyecto
![image](https://github.com/user-attachments/assets/a5c7c700-ee6d-47cd-bbb0-68efda6e42f4)

**"Automatiza tu infraestructura, simplifica tu gestión"**

**Título:** Automatización y despliegue de Infraestructura con Proxmox y Ansible.

**Descripción General:**  
Este proyecto se centra en la automatización del despliegue y gestión de infraestructura virtual utilizando Proxmox VE y Ansible. El objetivo es establecer una solución robusta y escalable que permita la creación, configuración y administración de máquinas virtuales de manera eficiente y reproducible.

---

## 2. Identificación del proyecto

- **Participantes:** Carlos Castillo González  
- **Ciclo formativo:** ASIR  
- **Centro educativo:** IES Albarregas  

---

## 3. Justificación y objetivos

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

## 4. Contenidos y aspectos principales

### Funcionalidad que se Implementará:

- **Instalación de Ansible en el Servidor Físico:** Configuración del servidor físico para ejecutar Ansible.  
- **Despliegue de Proxmox VE:** Instalación y configuración de Proxmox VE utilizando Ansible.  
- **Automatización con Ansible:** Creación de playbooks de Ansible para automatizar el despliegue y configuración de máquinas virtuales en Proxmox.  
- **Gestión de Máquinas Virtuales:** Configuración de almacenamiento y redes, creación de plantillas de VMs, y despliegue de varias VMs con diferentes configuraciones.  
- **Monitorización y Mantenimiento:** Implementación de herramientas de monitorización para supervisar el estado de las VMs y el servidor Proxmox.

### Cómo se va a Implementar:

**Instalación de Ansible en el Servidor Físico:**

- Instalar Ansible en el servidor físico desde el cual se gestionará toda la infraestructura.  
- Configurar el entorno de Ansible y preparar los playbooks necesarios.

**Despliegue de Proxmox VE:**

- Descargar e instalar Proxmox VE en el servidor físico utilizando Ansible.  
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

## 5. Medios que se utilizarán

### Arquitectura de Desarrollo:

- **Sistema Operativo del Servidor:** Proxmox VE basado en Debian.  
- **Lenguaje de Servidor:** Bash para scripts de configuración y Ansible para la automatización.  
- **Lenguaje de Cliente:** No aplica directamente, pero se podrían utilizar herramientas de administración web para Proxmox.  
- **Framework:** Ansible para la automatización.  
- **Sistema de Gestión de Bases de Datos (SGBD):** No se requiere un SGBD específico para la configuración inicial, aunque se puede utilizar MySQL o PostgreSQL para aplicaciones específicas dentro de las VMs.  
- **Herramientas de Monitorización:** Se podrían utilizar herramientas como Prometheus y Grafana para supervisar el estado de las VMs y el servidor Proxmox.  
- **Control de Versiones:** Git para el versionado de los playbooks de Ansible y scripts de configuración.

---

## 6. Áreas del ciclo formativo

- Implantación  
- Administración de sistemas  
- Redes  

---

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

## 9. Esquema del despliegue

*![image](https://github.com/user-attachments/assets/a950c848-e72c-4f0e-a3fb-364b3f08e394)*

---

## 10. Desarrollo

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
![image](https://github.com/user-attachments/assets/c42078e8-1a9f-4255-90b8-232bce4c8cad)

Ahora, instalaremos las dependencias necesarias para que Ansible interactúe con Proxmox:

```bash
ansible-galaxy collection install community.general
```

Instalamos también `proxmoxer` y `requests` haciendo uso de pip, pero primero, instalamos `venv`, el cual nos proporcionará un entorno virtual para Python:

```bash
sudo apt install -y python3-venv
```

Creamos el entorno:

```bash
python3 -m venv myenv
```

Lo activamos:

```bash
source myenv/bin/activate
```

Instalamos los paquetes:

```bash
sudo pip3 install proxmoxer request
```

Si nos da error esto, lo instalaremos mediante paquetes de Ubuntu:

```bash
sudo apt install -y python3-requests python3-proxmoxer
```

Aquí tendríamos nuestra máquina Ansible, en la cual realizaremos diferentes playbooks e inventarios para gestionar el despliegue.
![image](https://github.com/user-attachments/assets/252faf9c-2cc8-406e-ae94-23d30b9883f5)

---

### 3. Instalación de Proxmox:

Descargaremos la ISO de Proxmox desde su página oficial y crearemos una máquina virtual tal que así:

*![image](https://github.com/user-attachments/assets/7e4ecee8-2be2-4a31-8231-be7e4f3ea151)*

Una vez creada, la instalaremos. Aunque antes de instalarla, le agregaré una red interna para que se pueda conectar con la máquina Ansible. En la instalación, nos requerirá una IP la cual será la de nuestra red interna, en mi caso la `192.168.100.3`.

Una vez instalada, borramos el disco de instalación.

---

### 4. Instalación Ubuntu Cliente:

Instalaremos un Ubuntu cliente para así poder acceder a la interfaz de Proxmox y realizar nuestras configuraciones. Una vez instalado el Ubuntu cliente y configurada la red interna, nos dirigimos a Internet y ponemos:

```
http://192.168.100.3:8006
```

![image](https://github.com/user-attachments/assets/0cedb007-35a1-4d5d-b6a1-bdd004b9abfd)


Una vez logueados, ya tendríamos disponible nuestra interfaz de Proxmox, la cual trataremos de utilizar lo menos posible ya que con Ansible, podremos gestionar la mayoría de las operaciones a realizar para el despliegue, aunque sí tendremos que usarla para algunas configuraciones.

### 5. Creación de carpeta de trabajo:

Una vez ya instalado y configurado Proxmox, ya podemos comenzar con la preparación del despliegue de la primera máquina. Para ello, nos dirigimos a la máquina Ansible y creamos una carpeta para el trabajo:
*![image](https://github.com/user-attachments/assets/a45e3b75-8a5f-4496-baf7-968b8dcccff4)*
Una vez creada la carpeta, organizaremos los archivos necesarios en 3 partes:

- **Inventario**
- **Playbooks**
- **Cloud-init**

![image](https://github.com/user-attachments/assets/ed84593a-228f-484d-be81-93404573ed17)

### 5. Creación de Inventario:

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
![image](https://github.com/user-attachments/assets/63410708-1d6f-45ab-bfcf-599d112bc9ff)

### 6. Creación de Playbook:

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
### 7. Configuración Cloud-Init:

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
### 8. Subir imagen a proxmox:

Antes de ejecutar el playbook, debemos subir la imagen que tendrá la máquina que desplegaremos. Esto lo haremos mediante la interfaz gráfica.

Para ello, nos direigimos a la interfaz proxmox, seleccionamos el nodo, seleccionamos el almacenamiento, vamos a ISOS y cargamos la imagen previamente descargada:
![image](https://github.com/user-attachments/assets/c09288f3-0802-4f33-a65b-fd31d417c981)

### 9. Ejecutar playbook y confirmar despliegue:

Una vez preparados todos los archivos y la imagen, tendríamos todo listo para ejecutar el playbook y conseguir el despliegue de la primera máquina. Para ello, ejecutamos el comando siguiente:
```bash
ansible-playbook -i inventory.ini playbooks/snort.yml -u root --ask-pass
```
Con este comando, ejecutaremos el playbook que orquesta el despliegue como root.

### 10. Confirmación de la máquina:

Una vez terminado el despliegue, nos dirigiremos a la interfaz Proxmox para comprobar que todo ha sido creado correctamente:
- **Su configuración hardware**
![image](https://github.com/user-attachments/assets/9445eba3-eec3-4592-a47d-42cb9934b0e5)

- **Consola de la máquina**
  ![image](https://github.com/user-attachments/assets/b2517beb-1b7f-43df-aff6-44746f557d62)

- **Su IP y conectividad con Proxmox**
  ![image](https://github.com/user-attachments/assets/8f9eccab-bcd2-4f48-9c19-69f0a726362a)
  ![image](https://github.com/user-attachments/assets/421b1891-0a95-4d82-a400-42b0548d226b)

- **Comprobar si Snort está instalado**
  ![image](https://github.com/user-attachments/assets/0c7cd2ed-6745-4c6f-a768-c8cad462f80c)


  

