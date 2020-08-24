## Module 3 - Fundamentals Of Firewalls

### What is a Firewall
- uses one of these Methods
    - Packet filtering
    - Stateful packet filtering
    - User authentication
    - Client application authentication

### Types of Firewall
- **Packet filtering**
    - most basic and most common (though not most secure)
    - only packets that match the set criteria are allowed through.
    - many current OS includes these
    - also called screening firewalls
    - can filter based on **Packet size**, **Protocol used**, **Source IP addr** ...
    - work by examining a packet's **source addr**, **dest addr**, **source port**, **dest port** & **Protocol type**.
    - can either allow or deny (filtering rules)
    - only looks packet headers, has no info on payload.
    - doesnt track packets (no information on preceding packets), so cannot identify patterns based on traffic originating from single ip in bursts.(DoS attacks)

- **Application Gateway**
    - application proxy or application-level proxy. (WAF)
    - allows/denies certain specific types of apps
    - can act as web proxy
    - allows individual user authentication. quite effective in blocking unwanted traffic.
    - use a lot of system resources
    - susceptible to flooding attacks (Ping flood, SYN flood, etc) because,
        - it needs to negotiate/authenticate user/apps. 
        - it doesnt check the packets once connection is established.

- **Circuit level gateway**
    - same as application gateways, more secure and implemented on high-end equipments.
    - users are authenticated first and then connection to router is established (in appliction gateway its the other way around).
    - behaves like NAT, external systems never see internal systems.
    - more secure than others.
    
- **Stateful packet inspection**
    - SPI firewall is improved basic packet filtering, examines each packet and takes stateful decisions.
    - less susceptible to ping floods, SYN floods, less susceptible to spoofing.
    - capabilities
        - can identify if packet is part of abnormally large stream of packets from specific IP (identify DoS Attacks).
        - can identify spoofed IP (if source IP is internal)
        - can look at actual content of packet (can use advanced filtering capabilities)
    - recommended, becoming common
    - most home routers have option of using stateful firewalls


### Firewall Implementation, most used configurations include:

- **Network Host-Based**
    - also called host-Based
    - installed in the machine OS (host).
    - OS should be hardned, to avoid OS cofig/vulnarabilites causing security issues.
    - low cost (can use linux system as firewall)
    
- **Dual-homed**
    - runs on a server, with at lease 2 NICs.
    - older methodology, currently routers have FWs.
    - simply extended version of Host-based, server should be hardned.
    - relatively simple and inexpensive.

- **Router-based**
    - most routers has this option
    - in larger NW (with multiple layers), this is often first layer of protection.
    - most common fw in router is packet filtering.
    - can implement between subsections of NW. (reduces blast radius)
    - easy to setup. most home-routers have this
    
- **Screened host**
    - a combination of FWs.
    - a combination of a bastion host and a screen router.
    - a security flaw, a misconfiguration affects both FWs.


### Proxy Servers

- prevent hackers from seeing IP addresses of internal machines, NW configs. (NAT)
- control outgoing traffic. runs as SW on FW.
- can be configured to redirect certain traffic.

- **NAT**
    - provide security, by allowing connections that are originated on the inside nw.
    - can use inbound mapping (must be configured explicitly), to make some apps available to outside world.


### Windows firewalls

- are stateful packet inspection firewalls.
- windows10, can set different rules for outbound and inbound traffic.
- rules allow or block.
- can set rules for individual ports/applications.
- can apply rules differently depending on where the traffic comes from
    - **Domain**: for computers authenticated in domain.
    - **Public**: computers outside your NW.
    - **Private**: trafic from own computer.
- rules to follow:
    - block ports if not required.
    - block ICMP.
- logging, should be enabled.


### Linux firewalls
- **Iptables**
    - replaces ipchains. (/usr/sbin/iptables)
    - consists of
        - tables: contain chain of rules. (three tables, each as certain standard rule chains in it), can add custom rules. three tables are as below
          1. **Packet filtering** - is a packet filtering FW. contains. INPUT(processes incoming packets), OUTPUT(processes traffic sent out) and Forward (applies to routed packets) chains.
          2. **Network address translation** - used for NAT on outbound traffic, that initiates a new connection.  used only if machine serves as GW/Proxy.
          3. **Packet alteration** - used only for specialized packet alteration. called **mangle table**. contains 2 standard chains.
        - chains
        - rules

    - **Iptables Configuration**
    Basic config:
    ```
    iptables -F
    iptables -N block
    iptables -A block -m state --state ESTABLISHED,RELATED -j ACCEPT
    ```

    list:
    ```
    iptables -L
    ```

    save:
    ```
    iptables-save
    ```

    allow communication on specific port:
    ```
    iptables -A INPUT -p tcp -dport ssh -j ACCEPT
    iptables -A INPUT -p tcp -dport 80 -j ACCEPT
    ```

    Flags used:
    -A: Append this rule to rule chain
    -L: List the current filter rules
    -p: The connection protocol used
    --dport: dest port (single or range)
    -i: only match if packet is coming in on specified interface
    -v: Verbose
    -s, --source: source addresses
    -d, --destination: address destination spec.



#### Continue on to [Module 4 - IDS Concepts]()
