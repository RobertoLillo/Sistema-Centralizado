# Prototipo de sistema multiprotocolo moderno para la administración, autenticación y autorización de clientes en el Departamento de Ingeniería Informática.

Este repositorio contiene el proyecto de titulación para el semestre 1-2021 de la Universidad de Santiago de Chile, este recibe el nombre de ***Prototipo de sistema multiprotocolo moderno para la administración, autenticación y autorización de clientes en el Departamento de Ingeniería Informática*** y permite establecer un **sistema centralizado** al que se pueden conectar clientes de sistemas operativos Windows o Linux y aplicaciones Web o móviles, con el fin de consultar por autenticación y autorización de usuarios.

La forma de desplegar este sistema es mediante el *Playbook* de [Ansible](https://www.ansible.com/) que contiene el repositorio, que se encarga de levantar [Samba Active Directory](https://www.samba.org/) como servicio de directorio, [Keycloak](https://www.keycloak.org/) como punto de conexión entre distintas partes del sistema y finalmente integrando a [Google](https://developers.google.com/identity/protocols/oauth2/openid-connect) como proveedor de identidad para los usuarios de la universidad.

En una vista general, este playbook prepara los servidores actualizando el gestor de paquetes y la lista de *hosts* conocidos, instalando Docker y Docker-Compose, se desplegan en dos servidores distintos los servidores de Samba AD y Keycloak mediante Docker-Compose y finalmente se configura los sistemas de federación de usuarios y proveedores de identidad en Keycloak.
