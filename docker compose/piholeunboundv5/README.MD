This is for Pi-hole version 5.

Link to Pi-hole official site https://pi-hole.net/

Link to Pi-hole documentation for getting unbound setup https://docs.pi-hole.net/guides/dns/unbound/

Link to my youtube video showing this pihole-unbound.yml file being used with openmediavault https://youtu.be/IqsPH6oXy8c

CHANGE_TO_COMPOSE_DATA_PATH is a parameter used in openmediavault to specify the default container appdata path.

Credit to Pi-hole for the pihole container. I just added the unbound service to it.
I pull pihole/pihole container and proceed to add unbound service using a dockerfile. 

Dockerfiles are used to build your own containers.
