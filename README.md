# Asignacion final para el curso udemy Advanced Ansible
Desarrollo y procedimientos para la solución de la asignación del curso https://www.udemy.com/learn-ansible-advanced

# Plataforma/Infraestructura
Google Cloud Platform

# Entorno de desarrollo
Configuré una máquina virtual local en Oracle Virtual Box como mi controlador Ansible. Hay algunos requisitos previos necesarios en el sistema Ansible Controller para trabajar con Google Cloud. Los detalles están documentados aquí. Una vez que se configuró el controlador Ansible, procedí a desarrollar mi proyecto.

# Proyecto Ansible
Decidí usar el archivo de tasks para implementar VM y crear mis propios roles para configurar esas VM con Application.

- Tasks: una función para implementar las instancias informáticas necesarias en Google Cloud
- Roles: ansible-role-mysql: un rol para instalar y configurar MySQL en cualquier sistema dado
- Roles: ansible-role-flask-web: un rol para instalar y configurar la aplicación Flask en múltiples
- Tareas: configurar firewalls y balanceo de carga nativos de Google
- Tareas: enviar notificación por correo electrónico

Agrupar variables para tener las siguientes propiedades:

- project_id: ID de mi proyecto de GCP

- service_account_email: cuenta de servicio para conectarse a GCP

- credentials_file: archivo de credenciales para conectarse a GCP

- num_web_instances: número de instancias web para implementar

- db_name: nombre de la base de datos

- db_user: usuario de la base de datos para crear

- db_password: contraseña para el usuario de la base de datos

- machine_type: tipo de máquina para implementar, por ejemplo: n1-standard-1

- image: imagen de la instancia para implementar debian-7

- instance_list: una matriz que contiene la lista de servidores para implementar

   - web-server-1,web-server-2
   - db-server
   
- db_name: nombre de la base de datos

- db_user: usuario de la base de datos

- db_user_password: contraseña de usuario de la base de datos

- ansible_user: usuario para conectarse a las instancias de Compute mediante gcloud compute ssh

- ansible_ssh_private_key_file: archivo de clave privada para conectarse a las instancias de Compute mediante gcloud compute ssh

# Agradecimientos

Quiero Agraecer a todo el equipo de Toolbox, por darme la oportunidad de poder recibir este adiestramiento 
