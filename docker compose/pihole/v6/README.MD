This is for Pi-hole version 6 docker container. Alpine Based!

Link to Pi-hole official site https://pi-hole.net/

Link to my youtube video showing this pihole.yml file being used with openmediavault https://youtu.be/xpGfitMY-9c

CHANGE_TO_COMPOSE_DATA_PATH is a parameter used in openmediavault to specify the default container appdata path.

Creating a macvlan network in docker. Make sure to change subnet, gateway and parent(your primary network interface) to match your environment.

docker network create -d macvlan --subnet=10.0.0.0/24 --gateway=10.0.0.1 -o parent=ens18 local-network
