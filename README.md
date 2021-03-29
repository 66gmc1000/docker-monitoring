# docker-monitoring

docker create \
       --name=cups-airprint \
       --restart=always \
       --net=host \
       -v /var/run/dbus:/var/run/dbus \
       -v ~/.docker/airprint_data/config:/config \
       -v ~/.docker/airprint_data/services:/services \
       --device /dev/bus \
       -e CUPSADMIN="admin" \
       -e CUPSPASSWORD="password" \
       tigerj/cups-airprint
