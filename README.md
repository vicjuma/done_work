TECHNICAL REPORT
================

Introduction
------------

This project aims to implement a test rig for GigaTec-IT, a technology
services SME (small and middle-sized enterprises). It will demonstrate
the use of various technologies installation, setup, and administration.
For a robust test rig, we will use Cisco Packet tracer to simulate our
network prototype. Our network topology will include a DNS (domain name
system) server, database server, and a web server, a router, switches
and client devices. Later, the setup will be deployed on Ubuntu 18.04.6
LTS (Bionic Beaver) with the help of a virtualization software (VMware
Workstation 17 Pro). This setup reflects commonly used Linux-based
hosting environments which is characterized by high performance,
cost-effectiveness, and security.

### Aims, Objectives, and Deliverables

The main aim of this project is to create an inhouse web server
environment for GigaTec-IT's website, and user-data requirements.
Emphasis will be placed on compliance, security, and efficient resource
use. The objectives include the configuration of a web server, testing
data handing processes, setting up appropriate user roles, and providing
constructive feedback for network optimization. Key deliverables for
this project are:

-   A functional network environment prototype.

-   Fully configured web server for hosting GigaTec-IT\'s website.

-   Documentations involving user roles, network configurations, and
    compliance measures.

### Assumptions and Constraints

The implementation of this project was done will various considerations
and assumptions:

1.  **Host machine**: The implementation of the project will be done on
    a host machine running Linux-based operating system, which supports
    virtualization through VMware virtualization software.

2.  **Resource allocation**: Due to limited hardware resources,
    efficient RAM and storage will be configured to avoid
    overutilization while at the same time maintaining performance.

3.  **Virtual environment setup**: Linux-based OS is selected for its
    compatibility with open-source web server software like Nginx for
    web hosting, and MySQL for database services. This reflects industry
    standard configurations.

4.  **Security protocols**: Various security protocols like the TLS
    layer will be applied for encryption and secure communication
    alongside access permissions to secure the environment within the
    test rig, prioritizing data-protection and regulatory compliance.

Constraints to the project include limited physical network hardware. To
this extent, the test rig will leverage on the combination of virtual
network settings, and the currently available devices to simulate
connectivity and access. More advanced configurations like complex
firewall setups may not be fully implemented due to time and resource
constraints.

### Skills, Capabilities, and Available Resources

This project requires knowledge of operating systems (Linux-based),
service configurations, network design, network security, and web server
management. Resources will include a local machine, VMware
virtualization software, Ubuntu 18.04 ISO file, Nginx, and MySQL server
packages.

### Scope and Project Plan

The scope focuses on a simplified-yet-functional model of the company's
network infrastructure. It will incorporate essential components for web
hosting and data management. The project plan will incorporate:

1.  Setup of Ubuntu 18.04.6 LTS in a virtualized environment.

2.  Setting up and configuring a web server and a RDBMS to host
    GigaTec-IT\'s website.

3.  Implementing basic security and network configurations.

4.  Testing and documenting the essential system processes.

The creation of this test rig will facilitate GigaTec-IT to explore the
feasibility of a self-hosting solution, aligning with its strategic
goals.

Background Research
-------------------

To ensure reliability and efficiency and security of GigaTec-IT's
inhouse web server, it is necessary to evaluate underlying technologies.
This section will explore different architectures: different OS's
strengths, and weaknesses, fundamental networking functions, and
protocols. It will mainly focus on tailored solutions for SMEs like
GigaTec-IT. This research will also explore the relevant tools required
to set up and manage secure web environments.

### Operating Systems and Architecture

An appropriate operating system is integral to the overall operation of
a web server. This is because the OS contributes to system performance,
scalability, and security. Linux-based operating systems are widely used
in server environments due to their stability, strong community support,
compatibility, wide range of software packages, flexibility, and
customization (due to their open-source nature).

#### Linux-Based Operating Systems -- Ubuntu

Ubuntu is a Linux-based distribution derived from and building on Debian
foundation. Like most Linux distributions, it is an open-source OS. It
is regarded to its simplicity, and user-friendliness. As compared to
other Linux distros, it has extensive documentation, and updates. This
makes it suitable for new administrators and those prioritizing
stability for their development platforms. Debian, the distro where
Ubuntu is derived is known for its long-term stability and its advanced
package tool (APT) which is an extensive package management tool. Debian
and Debian-based distros also have robust security model making them
appropriate for enterprises requiring lightweight but secure kernel
solutions supporting TCP/IP stacks natively with tools such as
"iptables" for firewall configuration. This enhances security in web
hosting environments. Ubuntu and other Debian-based OS additionally
support essential server packages including Nginx, MySQL, and other
middleware required for hosting interactive web applications.

#### [Strengths of Linux OSs]{.underline}

-   Scalable and customizable due to their open-source property.

-   Strong support for open-source web/http server applications.

-   Extensive firewall configurations and other security features.

-   Active community support.

#### [Weaknesses of Linux OSs]{.underline}

-   Steep learning curve especially for administrators unfamiliar with
    > Linux environments.

-   Limited support for some commercial software and application
    solutions vis-a-vis Windows OS.

#### [Comparison with Windows Server]{.underline}

Windows server has a heavily reliant license cost as compared to Linux
which is not only free but also open-source. The high cost may not align
with GigaTec-IT's SME budget considerations. Notwithstanding the
attractive environment created by integrating Windows Server with
Microsoft SQL Server, open-source stacks web hoisting solutions with
Linux remain the preferred choice for flexibility, cost-effectiveness
and open-source compatibility.

#### [Network Architectures and Protocols]{.underline}

Traditional OSI model will be utilized for GigaTec-IT's test rig's
networking infrastructure. This will segment network functions into
seven distinct layers. Additionally, the more simplified TCP/IP suite
model will also be utilized in internet communications.

#### The OSI model and TCP/IP Suite

The Open Systems Interconnection (OSI) model is a conceptual framework
that breaks down computer network interactions into seven layers. These
layers are synchronized to create a digital message. The message is
built from the application layer to the physical layer. Nonetheless, in
practical applications, the TCP/IP suite is more widely adopted. This
suite contains four layers that streamline data communication across
networks, which makes it well-suited to web hosting. Some of the
application layers for GigaTec-IT protocols are:

-   HTTP/HTTPS - it plays a critical role in security and data
    encryption as far as data transmission between the web server and
    client devices is concerned.

-   DNS -- facilitates domain name resolution, an essential
    functionality that promotes accessibility and user-friendliness when
    navigating the company's web pages.

-   SSL/TLS - this protocol provides data protection with HTTP/HTTPS
    communication. This aligns with security and confidentiality of user
    data.

#### [IP addressing and Subnetting]{.underline}

Network segmentation is very important for traffic management, security,
and network efficiency. Efficient IP addressing and subnetting
facilitates this. We have utilized the IPv4 addressing scheme. Two main
primary subnets have been implemented: 192.168.1.0/24 and
192.168.2.0/24. The former subnet is used for servers and administration
while the later subnet is utilized for general employee access and other
peripherals. Tables 1 and 2 shows a summary of this information.

### **Table 1: Subnet 192.168.1.0/24**

  **Network**          **Device Type**             **IP Address**
  -------------------- --------------------------- ----------------
  **192.168.1.0/24**   Router Interface (Gig0/0)   192.168.1.1
                       DNS Server                  192.168.1.30
                       Database Server             192.168.1.20
                       Web Server                  192.168.1.10
                       CEO Computer                192.168.1.50

### **Table 1: Subnet 192.168.2.0/24**

  **Network**          **Device Type**       **IP Address**
  -------------------- --------------------- ----------------
  **192.168.2.0/24**   Router Interface      192.168.2.1
                       Employee 1 PC         192.168.2.2
                       Employee 2 PC         192.168.2.3
                       Employee 3 PC         192.168.2.4
                       Company Printer       192.168.2.5
                       Employee 4 PC         192.168.2.6
                       MD Laptop             192.168.2.2
                       Assistant MD Laptop   192.168.2.2

#### Network Security Mechanisms

Security is paramount in server environments. Data is a very important
resource, especially in this information age. The collection, and
storage and processing of user data should thus be done with security
consideration. Linux-based OSs have inbuilt firewall capabilities like
"ufw", and "iptables", which enable definition of rules by
administrators to control traffic and restrict unauthorized access.

#### [Firewall and Access Control]{.underline}

Both hardware-based and software-based firewalls can be used to segment
the network, and isolate sensitive services such as the database and DNS
servers from the less sensitive resources. ACLs (access control lists)
add an additional layer of protection by controlling traffic through IP
address restrictions and configuring specific user access. Some of the
strengths of firewalls are:

-   Allowing detailed control over outbound, and inbound network
    traffic.

-   User-level access controls can be supported through ACLs thus
    reducing the risk of unauthorized access.

#### [Data Encryption and Compliance]{.underline}

Encryption with additional TLS layer is very important. It prevents
attacks such as man-in-the-middle (MITM) attacks, an attack commonly
directed to sniff packets. This supports compliance with data protection
regulations. For compliance with GDPR, database encryption is also
essential to ensure secure data collection, processing and storage by
GigaTec-IT thus meeting industry standards.

#### Virtualization and Resource Optimization

Virtualization is a very important technology. It will enable GigaTec-IT
to cut on cost by running its test rig on a single physical host. This
optimizes resources and reduces costs. Using VMware, multiple VMs
(virtual machines) can run concurrently, each VM functioning as an
independent server with its own resource. Virtualization simplifies
management. Administrators are able to easily create VMs, save VM
snapshots, and delete VMs, allowing flexible and resilient test
environment. Some of the benefits of virtualization are cost
effectiveness especially for SMEs, and creation of isolated environments
which minimizes risks to the production network. Nevertheless, there are
performance limitations with virtualization as VMs compete for host's
resources. Multi-VM environments also require sophisticated
configurations to balance resources effectively.

#### Sustainability and Energy Efficiency Considerations

For sustainability initiatives, the reduction of energy consumption will
be appropriated through GigaTec-IT\'s implementation. Using
virtualization aligns with national sustainability practices by
minimizing the need for physical hardware. This in turn reduces energy
demand.

Leveraging Linux-based OSs. Virtualization, and secure network
architectures, GigaTec-IT can achieve scalable, secure, and
cost-effective web server infrastructure. These configurations will
support its operational objectives and facilitate secure and compliant
platform.

Pre-Engagement: Rig Design and Setup
------------------------------------

In this section, we will cover the design and setup of the test rig. We
will focus mainly on the mapping of business requirements to the network
design and configuration decisions. The rig will prioritize on security,
scalability, and compliance at the same time supporting a functional web
server, user management environment and network.

### Design Overview and Requirements Mapping

The test rig simulates a real-world network environment. The network has
two primary subnets. One subnet is utilized for core business servers
while the other is utilized for general employee access. This meets the
requirement for network segmentation for security purposes while meeting
smooth and reliable resource access.

#### Key Requirements

-   **Ubuntu 18.04 Server deployment**: An ubuntu server will be
    installed as the guest operating system to run the server software
    (Nginx), accessible by external clients. This server will host the
    SME's website and facilitate secure data management.

-   **Database server**: A database management system is essential for
    managing user data for the company's website. MySQL will be used
    because of its simplicity. Compared to alternatives solutions such
    as PostgreSQL, it is easier to implement. MySQL is also open-source
    making it ideal and cost effective as compared to some other
    solutions like Microsoft SQL Server.

-   **DNS server**: Handling domain name resolution into IP addresses to
    streamline access to resources both internally and externally

-   **User and device role assignments and segmentation**: specific
    subnets are used based on user roles. Access controls are also
    implemented for security compliance.

-   **Network security**: Inbuild firewall solutions will be utilized to
    restrict unauthorized access and encrypted connections implemented
    to ensure data protection.

-   **Virtualized environment**: VMware Workstation Pro is utilized for
    cost-effectiveness. Virtualization also facilitates flexible
    resource management and multiple VMs can be spined concurrently on
    the same physical host machine.

#### Setup Components and Network Layout

The rig components model is shown in figure 1 below which is a packet
tracer model. The setup was created to simulate how the devices will be
able to communicate. However, for the router and switches, physical
components are not are requirement. Therefore, virtual routers and
switches will used making the setup more cost effective.

### **Figure 1: Network Simulation Model with Cosco Packet Tracer**

Figure 1 showing some of the components used in the setup: web server,
database server, DND server, routers, and switches.

#### Practical Steps

The setup requires a series of steps including VMware Workstation and OS
installation, network configuration, and software setup on virtual
machines.

I.  A Debian-based host operating system was used in the rig setup. This
    makes for a powerful host machine that provides the base environment
    for running the virtualization software and installing the VMs for
    the web host setup.

II. Virtualization software. A bundle file was downloaded from the
    official website (https://www.vmware.com/) and the md5 file hash
    confirmed after download to confirm the integrity and authenticity
    of the file before installation. After verification, the terminal
    "chmod" command was utilized the add "execute" (x) permission to the
    bundle file and running the executable. Due to module (vmmon and
    vmnet) errors after installation, manual installation of these
    modules was done using the steps shown in figure 2

### **Figure 2: Manual Installation of VMware Modules**

III. Installing Ubuntu 18.04 live server. The ISO image downloaded from
     > <https://releases.ubuntu.com/18.04/> was used in the installation
     > process. In VMware Workstation 17 Pro, the create new virtual
     > machine option was selected and the live server ISO file selected
     > for installation. The basic configuration like user information,
     > machine name and resource allocation processes were carefully
     > configured and the installation done. Later openSSH server was
     > installed for secure communication between the server and other
     > host machines.

### Figure 3: Manual Installation of VMware Modules

> After the installation process, update and upgrades were done on the
> system server to ensure that all the packages are up to date for
> efficient running of the server.

IV. Setting up DNS server. The bind package was utilized for this
    > process with the setup shown in the figure 4 below. DNS server is
    > configured to perform domain name resolution to IP addresses
    > within the network. The setup not only improved accessibility but
    > also reduces reliance on external DNS services.

### Figure 4: DNS Setup using Bind9

V.  Nginx, Firewall, and MySQL Setup. Using the apt package manager,
    > these packages were installed and various configurations done as
    > summarized in the commands in figure 5. Nginx is installed and
    > configure to listen on ports 80 (HTTP) and 443 (HTTPS). SSL/TLS
    > certificates are important in the configuration to secure data
    > transmission. User privileges are configured on MySQL server to
    > restrict database access to only authorized users. Ufw software is
    > used to manage firewall rules allowing only necessary traffic.

### Figure 5: MySQL, Nginx, and Firewall Configurations

The pre-engagement process carefully considers GigaTec-IT\'s business
needs, sustainability goals, and technical requirements. The setup meets
the business' needs for compliance, sustainability, and security. This
in turn lays a strong foundation for continued development and
deployment.

Engagement
----------

This section evaluates the practical implementation of the solutions
used by GigaTec-IT's test rig. Comparisons will be drawn between the
different OS architectures, network configurations, and software
components. We will also explore the use of other server software like
MySQL, and Nginx that are essential to web and database servers.

### Comparison of OS Architectures

Various OS architectures were considered before settling for Linux
Ubuntu distribution. Even though Windows Server might present a
user-friendly interface with a presentable GUI (graphical user
interface), it is very expensive when it comes to its license. This may
not be feasible for SMEs such as GigaTec-IT. Debian-based distros also
have a large community making troubleshooting OS issues due to the large
number of online resources as compared to some other Linux distros.
Linux OSs are also more customizable as compared to Windows and macOS.

#### Key OS Components

-   Kernel: it handles memory management, networking and CPU scheduling.
    Due to its monolithic nature, it has the capacity to combine core
    functions within its kernel space, thus expediting high performance
    and efficient IPC (inter-process communication).

-   User space: It houses essential packages like Nginx, and MySQL.
    These processes are isolated thus enhancing security, and allowing
    the management of permissions and resource allocation.

-   Networking capabilities: robust networking features like firewall
    (ufw) support, IP routing, and support for several protocols are
    offered by Linux-based OSs.

Setup of the test rig involves the configuration of resources such as
RAM, CPU, and storage settings. Effective configuration ensures optimal
performance for the DNS, wen and database servers. Efficient resource
allocation is very critical especially in multi-VM environments.

Because of the processes (daemons) that would be running on the Ubuntu
server, a dual core CPU allocation with 4GB RAM is necessary for
effective performance. The web server software handles HTTP requests and
sends responses, it processes PHP scripts, making sufficient allocation
of these resources crucial to avoid latency. Server environments are
characterized by processes running in the background called daemons.
These processes will include all the services currently in the test rig
setup. A higher memory will thus be required especially due intensive
data processing involving the database server.

#### Components Installation

1.  Nginx configuration. After installation, nginx must be configures to
    serve webpages. An advantage of Nginx is that it can also act as a
    reverse proxy. Nginx configuration files are placed inside the
    "sites-available" folder in the "/etc/nginx/" directory. For
    GigaTec-IT configuration, the configuration will be located in the
    directory "/etc/nginx/sites-available/gigatec-it.local" and the
    server block populated with the necessary configuration. With a
    fully registered domain name, lets encrypt package can be used to
    acquire certificates for secure layer (TLS).

2.  MySQL database. PhpMyAdmin is normally used as an interface for
    interacting with the database. It provides a user-friendly GUI that
    streamlines the management of user data. However, these GUI
    applications normally take a lot of space which may not be
    available. They are also dependent on desktop environment that may
    further consume a lot of resources. Doe to this, the terminal-based
    MySQL server is better and cost effective. User roles and privileges
    in MySQL restrict access to data facilitating compliance with data
    privacy standards.

3.  PHP. It is a scripting language used to render dynamic content on
    the website. It integrates with MySQL database facilitating data
    retrieval and storage. Configurations stored on the web server are
    optimized to prevent excessive memory usage. These configurations
    direct the execution of PHP scripts stored in the web server.

4.  Command line interface (CLI). In server environments, most tasks and
    configurations are done via the CLI. This provides direct control
    over system resources and configuration files. Creating users with
    their various roles, performing installations, managing files and
    directories leverage the CLI. In the creation of the test rig,
    installation of all the tools, configurations, and management were
    all done via the CLI. As much as the GUI offer a user-friendly
    environment, additional resources (CPU, RAM, and storage) are
    required to keep them up. Furthermore, server environment does not
    always require such application because they are normally operated
    by system administrators who have a high level of expertise as
    compared to desktop environment which are normally used by people
    with little to no knowledge of the underlying configurations.

#### Network Configuration: OSI and TCP/IP Models in Practice

These two are foundational frameworks for understanding network
communication within the test rig's setup. The OSI model is composed of
seven layers:

1.  Physical layer (layer 1) - virtual network interface cards through
    VMware's virtualization environment

2.  Data link layer (layer 2) - in VMware, these are represented through
    the different network configurations which are created automatically
    during installation. There are three major virtual switches (VMnet):
    VMnet0 (bridged), VMnet1 (Host-Only), and VMnet8 (NAT). They are
    configured via the **Virtual Network Editor** tool in VMware
    Workstation.

3.  Network layer (layer 3) - managed by routing, network adapters,
    virtual switches, and ufw access rules to restrict traffic.

4.  Transport layer (layer 4) - Managed by protocols, and services
    running in the VMs themselves. TCP secures data transfer and ensures
    reliable delivery.

5.  Application layer (layer 7) - service protocols like HTTP for the
    HTTP web server and DNS operate at this layer. There is direct
    interaction between these protocols with user requests and data.

The TCP/IP suite on the other hand is composed of four layers:

1.  Network access -- Handle local data delivery, emulating layers 1 and
    2 of the OSI

2.  Internet layer - corresponds to the network layer of the OSI. It is
    responsible for routing and IP addressing.

3.  Transport -- Manages connection via TCP for HTTP connections and
    also secures data flow.

4.  Application -- the end-user interacts directly with this layer. It
    hosts the DNS, web, and database services

#### Protocol Analysis and Security

**HTTP** (Hypertext Transfer Protocol) and **HTTPS** (secure Hypertext
Transfer Protocol). The former is normally used to test local
environment and loopback interfaces (127.0.0.1). Due to possibilities of
attack, an additional secure layer (TLS) was added through certificate.
This enables data encryption during transmission from the source to the
destination. HTTPS is used for this encryption. Encryption is a
necessity for compliance with data protection measures. **DNS** on the
other hand operates over UDP. Allows hostnames resolution. Firewall ACLs
restrict access to specific services. Refined ACLs allow only authorized
devices and protocols.

#### Virtualization and Network Types

By using VMware, multiple VMs can be hosted on a single physical device.
This allows for isolated test environment for each guest device.
Virtualization has several benefits. It facilitates resource
optimization as it maximizes on the use of RAM, CPU, and storage, thus
reducing hardware requirements and energy consumption making it
cost-effective. With multiple VMs, each server runs in its own isolated
environment thus reducing dependency on physical hardware. Scalability
is also easier will virtualization as new VMs can be easily added as
business requirements continue growing to scale the network. There are
two main network types relevant to the implementation of our test rig;
local area network, and virtual private network. The latter is not
implemented although it may connect remote users securely.

#### Real-World Considerations

Data encryption via the HTTPS protocol which has an addition TLS layer
makes the system comply with GDPR requirements. Some of the security
practices implemented are encryption via SSL/TLS certificates thus
preventing the common MITM attack. Access logging enables auditing and
command history for security tracking. Regular patching also happens
with most Linux-based distributions. Regular updates and upgrades are
always done to protect against potential vulnerabilities. Sustainability
comes in through the reduction of energy consumption and efficient use
of available resources.

Post Engagement
---------------

This section summarizes the outcome of the test rig, evaluating
performance and discussing any observed limitations. There are also
recommendations for future improvements.

### Summary of Work and Key Deductions

GigaTec-IT test rig demonstrates the effectiveness of virtualization to
support essential business functions like data processing, web hosting
and DNS management. Using Ubuntu in combination with Nginx, PHP, and
MySQL facilitates a complete company stack for its service needs. The
test rig setup confirmed that virtualization could also handle the
network aspect of the business-like web and data transactions for SMEs
at sufficient speeds. Allocated storage, CPUs, and RAM were sufficient
for the current scope as was indicated through testing.

Marginal delays were however observed with higher simulated traffic
loads. For data security and compliance, successful implementation of
the SSL/TLS certificate installation on the web server restricted
database access. Robust use of ufw firewall configurations demonstrated
compliance with the GDPR and other data privacy standards.
Sustainability is leveraged by virtualization in reducing the need for
more physical hardware. This minimizes power, and energy consumptions,
and also reduces the required operational space sustainability, which
aligns with GigaTec-IT\'s sustainability objectives.

Limitations and challenges were however observed. Resource constraints
especially in multi-VMs. Because the VMs compete in the host machine's
resources, performance can be affected especially if multiple VMs are
running concurrently. Scalability might pose a challenge. Although the
current setup works, upgrade are necessary as user-base grows as
horizontal scaling (installing more VMs) may not contribute to the
success of the company when it scales.

Data redundancy is also a challenge for the current setup. Due to the
absence failover strategies and automated backups, the system is
vulnerable to downtimes or data lose in the event of system failures.
Integrating backups and data recovery measures would improve data
resilience.

### Recommendations for Improvement

Scalability is almost unavoidable with most businesses. Preparing for it
is this imminent. Adopting clod-based services like AWS and Azure will
facilitate dynamic resource scaling. Notwithstanding the current ACLs in
the setup, multi-factor authentication should also be considered to
improve the overall security of the system. Other security
considerations include and intrusion detection system and automated
patch management. Data redundancy is an important aspect for businesses
as it facilitates data resilience. Implementing daily database backups
and weekly snapshots would facilitate data integrity and operational
continuity.

Additionally, advanced storage configurations such as RAID should also
be adopted to mitigate against hardware failures. Continual improvement
improves business' relevance. This can be enhanced through real-time
performance monitoring. Tools such as Prometheus could be adopted to
assist the IT team to proactively allocate and manage resources, thus
addressing performance issues before impact on the user experience. For
sustainability, GigaTec-IT could consider sourcing renewable energy for
its operations.

### Self-Reflection and Project Impact

Valuable insight was gained in the process of creating the GigaTec-IT's
test rig. Insights into network configurations, security,
virtualization, and OS was gained in the process. This project
demonstrated on SMEs could adapt to Linux-based solutions with
virtualization technology. This post-engagement phase evaluated
project's outcomes, and areas of improvements.

Appendix
--------

### Networking Devices Security Measures

  **Device Type**    **Compliance/Security Measures**
  ------------------ --------------------------------------------------------------------
  Router Interface   Firewall configured
  DNS Server         Regular updates, DDoS protection
  Database Server    Encryption for data storage, access control
  Web Server         SSL certificate, secure protocols
  All Employee PCs   User authentication, antivirus software, network security measures

### Various Technologies with Detailed Sustainability Measures

  **Sustainability Measures**   **Details**
  ----------------------------- --------------------------------------------------------
  Energy-Efficient Hardware     Use of energy-efficient servers and switches
  Virtualization                Implement virtualization to optimize resource usage
  Cloud Backup                  Utilize cloud solutions for data backup and redundancy

### Hosting a PHP Website with Nginx and MySQL

i)  Installation of Nginx, confirming its installation, and managing its
    daemon:

ii) Installing PHP and MySQL Server.

> Installing ssl certificate using openssl for local environment
>
> Making requests to the domain name
