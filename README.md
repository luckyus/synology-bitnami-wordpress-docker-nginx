# synology-bitnami-wordpress-docker-nginx
To run bitnami's docker image for wordpress (nginx version, not apache) at my church's synology DS216+II, with only 1024M ram (i think that's why the apache version doesn't work)
- https://github.com/bitnami/bitnami-docker-wordpress-nginx

## Notes
- need to add folder ./certs and add the cert files (server.crt & server.key) to the folder
- set user: '1024:0' to allow mounting to host directories '/volume1/docker/admin_wordpress_data' & '/volume1/docker/admin_mariadb_data' to '/bitnami/wordpress' & '/bitname/mariadb' resp.
- 'user: root' also works
- removed the original two docker volumes mariadb_data & wordpress_data
