BGP ISP Network Architecture Simulation
Multi-Domain Routing & Inter-ISP Connectivity
📌 Project Overview
This project is a high-fidelity simulation of an Internet Service Provider (ISP) backbone using Border Gateway Protocol (BGP). Developed in Cisco Packet Tracer, the architecture models three independent Autonomous Systems (AS) exchanging routing information to provide end-to-end connectivity between geographically dispersed LANs and a central Web Server.

As the Founder of the Networking and Cybersecurity Lab at Mama Ngina University, I developed this project to demonstrate the practical application of inter-domain routing in enterprise-scale environments.

🏗️ Network Topology
The simulation consists of three distinct ISP environments:

ISP A (AS 100): Represents a regional provider managing a local client subnet.

ISP B (AS 200): Acts as the transit hub/core provider facilitating communication between AS 100 and AS 300.

ISP C (AS 300): Hosts the enterprise Web Server and critical internet resources.

🛠️ Technical Implementation
Protocol: External BGP (eBGP) for inter-AS routing.

Addressing: Implemented a VLSM-based IPv4 addressing scheme for serial point-to-point links and GigabitEthernet LAN interfaces.

Routing Logic: Configured BGP neighbor adjacencies and utilized the network command to advertise local prefixes across the BGP table.

Automation: Leveraged automated configuration scripting to ensure consistent peer-to-peer peering.

🚦 Verification & Troubleshooting
To ensure a fully converged network, the following verification commands were utilized:

show ip bgp summary: Verified that all BGP neighbors reached the Established state.

show ip route: Confirmed that BGP routes (marked with 'B') were successfully injected into the global routing table.

End-to-End Ping/Tracert: Validated ICMP connectivity from PC-A (AS 100) to the Web Server (AS 300).

📁 Repository Structure
/topology: Contains the .pkt (Cisco Packet Tracer) source file.

/configs: Text files containing the running configurations for each ISP router.

/screenshots: Visual proof of network convergence and routing tables.
