# Client-Server Architecture in Linux Environments

## 1. Core Learning Points

Through this study and practical lab, I have explored the fundamental relationship between clients and servers in a distributed system.

* **Architectural Roles:** I learned that the **Server** is a high-availability host that "listens" for requests and manages centralized resources (like a MySQL database), while the **Client** is the service consumer that initiates communication.
* **Linux Service Management:** I practiced using `systemctl` to manage background daemons. In Linux, a server is essentially a process (like `mysqld`) that remains active to handle incoming network packets.
* **Network Security & Scoping:** I explored the importance of **Firewalls (Security Groups)** and **Bind Addresses**. I learned that even if a service is running, it must be explicitly told to listen on a network interface (`0.0.0.0`) rather than just the local loopback (`127.0.0.1`).
* **Decoupling Services:** By separating the database client from the server, I realized how modern applications scale. One database server can serve multiple client instances, improving resource efficiency.

---

## 2. Practical Implementation: MySQL Remote Connectivity Lab

### Project Overview

This project demonstrates the implementation of a **Client-Server Architecture** using two remote AWS EC2 instances. One instance is configured as a dedicated **Database Server** running MySQL, and the other acts as a **Database Client**. This setup provides hands-on experience with remote database connectivity, networking security, and firewall configuration.