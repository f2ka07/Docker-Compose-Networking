# Docker-Compose-Networking
## External networks in Docker Compose

The **Docker Compose external network** denotes a feature in Docker Compose that enables you to link your Compose-managed containers to an existing network that is external to the Compose project. As a default, any network created in Docker Compose is only discernible to the containers within that particular Compose project. Nonetheless, using the "external" keyword in your Compose file permits the connection of Compose-managed containers to an external network. This functionality proves valuable in cases where you need to establish communication between multiple Compose projects or when you intend to connect your Compose-managed containers to a network managed by a distinct tool or system.

## Docker Compose network host

**Docker Compose network host** is a networking mode in Docker Compose that allows containers to share the same network namespace as the host system. In this mode, the containers' network interfaces are mapped directly to the host system's network interfaces, and they share the same IP address as the host system.

When you specify the "network_mode: host" in your Docker Compose file, Docker Compose will not create a new network for your containers. Instead, it will use the network stack of the host system, making the containers appear as if they are running directly on the host system. This networking mode is useful for situations where you need to access services that are only available on the host system or when you want to avoid the performance overhead of using a separate network stack.

It's worth noting that using the "network_mode: host" option in Docker Compose may have security implications, as it grants the container access to all network services running on the host system. Therefore, it's recommended to use this mode only when necessary and to carefully consider the security implications.


