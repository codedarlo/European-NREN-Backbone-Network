# EUROPEAN NREN BACKBONE NETWRORK. 
## OVERVIEW 
Simulation of a GEANT-style European NREN backbone with segregated R&amp;E, Internet, and LHCONE traffic using VLANs, dynamic routing, DHCP, NAT, and security controls.
The network interconnects multiple National.
Research and Education Networks (NRENs) using a shared, high-capacity TCP/IP
backbone while enforcing strict traffic segregation and security controls.

The design supports three distinct traffic classes:
- Research & Education (R&E)
- Internet Access Service (IAS)
- LHCONE (Large Hadron Collider)

Each traffic type is isolated at both Layer 2 and Layer 3 to ensure performance,
security, and policy compliance, reflecting real-world carrier and service
provider networking practices.

## High-Level Network Design
The backbone network is designed to theoretically support connectivity for
42 independent NRENs, each operating as a separate Autonomous System (AS)
and peering with GEANT at Provider Edge (PE) routers.

The design considers:
- Scalability and future growth
- Redundancy and resiliency
- Cost-aware infrastructure decisions
- High-capacity Ethernet links (100Gbps minimum)
- Integration with Tier-1 Internet Service Providers

## Traffic Segmentation Model
The network enforces strict multi-tenant separation using VLANs and routing
policies:

### Research & Education (R&E)
- Dedicated VLAN per site
- Fully routed traffic between sites
- Supports inter-university collaboration

### Internet Access Service (IAS)
- Dedicated VLAN
- Static default route towards ISP cloud
- Inter-site communication blocked using ACLs

### LHCONE
- Dedicated VLAN for high-performance scientific traffic
- Fully isolated from IAS and external traffic
- Optimised for large-scale data transfer

## Simulation Scope
To validate the design, a representative subset of the network is simulated
using four sites:

- Cambridge (GEANT core site)
- Amsterdam (GEANT core site)
- Frankfurt (NREN customer site)
- Paris (NREN customer site)

Each site contains:
- Three VLANs (R&E, IAS, LHCONE)
- DHCP-based host addressing
- Dynamic inter-site routing
- End-to-end connectivity testing

## Operational & Security Considerations
- Private IPv4 addressing with NAT for external connectivity
- SSH-only remote management on all network devices
- VLAN and ACL-based traffic isolation
- Budget-conscious design decisions
- Security-first configuration principles

## Repository Contents
- **Network_Design_Report.pdf** – Full technical documentation
- **Network_Presentation.pdf** – Summary slides for stakeholder presentation
- **Device_Configurations.txt** – Router and switch configuration commands
- **Verification_and_Testing.md** – Connectivity and configuration verification
- **IP_Addressing_Plan.xlsx** – Structured IPv4 addressing using VLSM
- **Secure_Enterprise_Network.pkt** – Cisco Packet Tracer simulation file


## Skills Demonstrated
- Private IPv4 addressing with NAT for external connectivity
- SSH-only remote management on all network devices
- VLAN and ACL-based traffic isolation
- Budget-conscious design decisions
- Security-first configuration principles
