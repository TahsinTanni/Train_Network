# Train_Network
A fully designed and configured Cisco Packet Tracer network for Transport for New South Wales (TfNSW), modeling the Sydney Trains digital modernization project.

This repository contains the full network design and configuration for Transport for New South Wales (TfNSW) as part of their Sydney Trains digital modernization initiative. The project models six high-traffic stations and establishes a secure, high-speed communication network to support operational coordination, staff devices, digital displays, ticketing systems, and public Wi-Fi for commuters.

## 🚉 Stations Included

| Station       | Daily Users |
|---------------|------------|
| Central       | 3200       |
| Town Hall     | 2800       |
| Wynyard       | 2400       |
| Redfern       | 1500       |
| Burwood       | 1300       |
| Parramatta    | 2600       |

## 🛠 Project Features

- Core network hub at Central Station
- Direct connections among Central, Town Hall, Wynyard, and Redfern for critical routes
- Cost-optimized connectivity for Burwood and Parramatta via Redfern
- VLSM-based subnetting for minimal IP wastage
- Static IP for Central and Wynyard; DHCP for other stations
- DHCP, DNS, Web, and Email server deployment
- Manual server IP configuration
- Static routing for Central, Town Hall, Wynyard
- Dynamic routing (RIP v2) for Redfern, Burwood, Parramatta
- Redundant backup link between Central and Wynyard
- Full end-to-end connectivity tested
- Local PCs and printers at each station for realistic simulation

## 📂 Repository Structure
├── topology-diagram.png # Network topology diagram with labeled routers, servers, and links
├── Sydney_Trains_Network.pkt # Cisco Packet Tracer project file
├── router-configs/ # Folder containing all router configuration commands
│ ├── Central.txt
│ ├── TownHall.txt
│ ├── Wynyard.txt
│ ├── Redfern.txt
│ ├── Burwood.txt
│ └── Parramatta.txt
├── vlsm-subnets.xlsx # VLSM subnetting calculations
├── ip-addressing-table.xlsx # Complete IP addressing table for devices and interfaces
└── assumptions.md # Document listing all assumptions made during network construction

## 📖 Usage

1. Open in Cisco Packet Tracer.
2. Verify connectivity between stations using ping tests.
3. Access the web service by typing `www.sydneyrail.net` in any station PC browser.
4. Review router configurations in `router-configs/`.
5. Check IP assignments and subnet calculations in the provided spreadsheets.

## 💡 Notes

- All routing configurations strictly use static and RIP v2 protocols; no default routes are applied.
- Central Station functions as the main DHCP and DNS server.
- Parramatta hosts the network's email server.
- Wynyard and Central include redundant backup links for high availability.


