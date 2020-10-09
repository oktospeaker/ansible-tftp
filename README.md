# ansible-tftp
Deploy docker container with TFTP-server based on vimagick/tftpd (https://hub.docker.com/)

## Role variables
| Variable | Default value | Description |
| :---:        |     :---:      |         :---: |  
tftp_service_name               |       tftp-docker             |   Service name in OS
uninstall_service               |       false                   |
tftp_host_port                  |       69                      |   Host network port for service
tftp_container_port             |       69                      |   Container network port for service
tftp_port_type                  |       udp                     |   Type of port (tcp/udp) for service
host_dir                        |       /var/docker/tftpboot    |   Mapping directory on host
container_dir                   |       /tftpboot               |   Mapping directory on container
docker_image                    |       vimagick/tftpd          |   Docker image (https://hub.docker.com/)

### How to use
    - installation: just start the role
    - uninstallation: add --extra-vars "uninstall_service=true" (WARNING: It doesn't delete directory /var/docker/tftpboot on host!!)
