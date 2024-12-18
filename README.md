
## Raspberry Pi 5 Home Lab Server Log

---

### Descripción general del sistema
- **OS:** Open Media Vault (OMV) - Linux (Debian-based)
- **Fecha de instalación:** 09-10-2024
- **Algunos paquetes preinstalados que vienen con OMV**:
  - **Docker**: Container manager para virtualización
  - **Python**: v3.11.2
  - **rsync**: Utilidad de transferencia y sincronización rápida de archivos
  - **cron**: Tareas programadas, para automatizar tareas

- **NTP Time Server**: Necesario porque la raspberry Pi no tiene RTC (reloj en tiempo real) integrado
  - **Configruación**: Network Time Protocol (NTP) instalado y configurado para un registro hora preciso
  - **Cronjob Setup**: Se inicia automáticamente al reiniciar 
  - **Referencia**: [NTP Setup on Raspberry Pi](https://forums.raspberrypi.com/viewtopic.php?t=308207)

**Nota**: _Siempre que sea posible, preferir los contenedores Docker en lugar de las instalaciones directas por su simplicidad y facilidad de mantenimiento._

---

### Paquetes instalados (a través de `apt install o curl`)

| Package        | Fecha de Instalación | Descripción                                                                                                   |
|----------------|-------------------|---------------------------------------------------------------------------------------------------------------|
| **plex media server** | 09-10-2024        | !Instalación provisoria; migrar a contenedor Docker           |
| **noip-duc**           | 15-10-2024       | Dynamic DNS Update Client para mantener una dirección IP actualizada para el acceso externo [No-IP](https://www.noip.com/) |
| **git**                | 05-11-2024       | git es git                     |
| **VS Code**            | 06-11-2024       | VS Code                     |

---

### Docker Containers

| Container | Fecha de Instalación | Descripción                 | Info                                             |
|-----------|-----------|---------------|------------------------------------------------------------|
| **portainer** | 16-10-2024 | Docker manager GUI | [Portainer](https://www.portainer.io/)                     |
| **homepage**  | 07-10-2024 | Server dashboard      | [Homepage](https://gethomepage.dev/)                       |
| **NextCloud** | 12-10-2024 | Self Hosted Personal Cloud      | [NextCloud](http://https://nextcloud.com/)                     |

---

### Server Roadmap

1. **Install Nginx**: Multi-functional server for HTTP, reverse proxy, caching, load balancing, and proxy services. [web nginx](https://nginx.org/en/)
2. **Torrent Client**: Instalar algún cliente torrent, probablemente qbitorrent
3. **AI Server Setup**: Instalar servidor de IA, considerar los límites de la Raspberry Pi 5
