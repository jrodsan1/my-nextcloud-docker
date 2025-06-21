<<<<<<< HEAD
# my-nextcloud-docker
Nube personal con Nextcloud con acceso desde fuera.
=======
# Nube personal con Nextcloud usando Docker

Este repositorio contiene la configuración para desplegar una nube personal con Nextcloud usando Docker, MariaDB y Nginx, junto con instrucciones para instalar Docker y preparar el entorno.

---

## Índice

1. [Requisitos previos](#requisitos-previos)  
2. [Instalación de Docker y Docker Compose](#instalación-de-docker-y-docker-compose)  
3. [Configuración del proyecto](#configuración-del-proyecto)  
4. [Crear y personalizar docker-compose.yml](#crear-y-personalizar-docker-composeyml)  
5. [Levantar los contenedores](#levantar-los-contenedores)  
6. [Acceso y configuración de Nextcloud](#acceso-y-configuración-de-nextcloud)  
7. [Mantenimiento y actualizaciones](#mantenimiento-y-actualizaciones)  

---

## Requisitos previos

- Sistema operativo Ubuntu (o similar Linux) actualizado.  
- Usuario con permisos sudo.  

---

## Instalación de Docker y Docker Compose

### Instalar Docker

```bash
sudo apt update
sudo apt install -y ca-certificates curl software-properties-common
curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo gpg --dearmor -o /usr/share/keyrings/docker-archive-keyring.gpg
echo \
  "deb [arch=$(dpkg --print-architecture) signed-by=/usr/share/keyrings/docker-archive-keyring.gpg] \
  https://download.docker.com/linux/ubuntu $(lsb_release -cs) stable" | \
  sudo tee /etc/apt/sources.list.d/docker.list > /dev/null
sudo apt update
sudo apt install -y docker-ce docker-ce-cli containerd.io
sudo systemctl enable --now docker
