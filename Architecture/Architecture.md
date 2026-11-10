

## Networking System Assets

we will use a 10.0.0.0/8 class-A corporate network space divided into strict functional VLANs.

**Function of VLan's:** 


|     **Asset / Device**    | **VLAN** | ****Internal IP** Address (Office)** | ****MAC Address****   | **Hostname**   | **Function**                                 |
|:-------------------------:|:--------:|----------------------------------|-------------------|----------------|----------------------------------------------|
| Core Firewall             | VLAN 10  | 10.10.1.1                        | 00:50:56:A1:B2:C3 | CORP-FW-01     | Perimeter Defense / Boundary Gateway         |
| Perimeter IPS             | VLAN 10  | 10.10.1.2                        | 00:50:56:A1:B2:D4 | CORP-IPS-SNORT | Deep Packet Inspection Engine                |
| Core Router               | VLAN 10  | 10.10.1.254                      | 00:50:56:A1:B2:E5 | CORP-RTR-01    | Inter-VLAN Routing & Switching               |
| Internal Server Container | VLAN 20  | 10.20.1.10                       | 00:50:56:B2:C3:D4 | CORP-SRV-APP01 | Internal Active Directory & Web Applications |
| Perimeter Proxy Server | VLAN 70 (DMZ)  | - 10.70.1.10 (Internal) - 203.0.113.5 (Public Facing)                       | 00:50:56:C3:D4:E5 | CORP-SRV-APP01 | DMZ-PROXY-NGINX	Asynchronous Nginx Gateway  |


		
		



---

## 🏢  Corporate Asset Directory & Personnel Registry

### Upper Management (V-Lan 30)

**Network Profile:** Allowed to connect via Corporate Office Ports or secure Corporate VPN when working from home.

1. **Director**

- **Email:** director@corp.local
- **Hostname:** MGMT-DIRECTOR-L (Laptop)
- **Internal IP** (Office): 10.30.1.10
- Home/VPN IP Range: 172.16.30.10
- **MAC Address**: 00:E0:4C:3A:11:AA

2. **Executive**

- **Email:** executive@corp.local
- **Hostname:** MGMT-EXEC-L (Laptop)
- **Internal IP** (Office): 10.30.1.11
- Home/VPN IP Range: 172.16.30.11
- **MAC Address**: 00:E0:4C:3A:11:BB

3. **HOD (Head of Departments)**

- **Email:** hod@corp.local
- **Hostname:** MGMT-HOD-L (Laptop)
- **Internal IP** (Office): 10.30.1.12
- Home/VPN IP Range: 172.16.30.12
- **MAC Address**: 00:E0:4C:3A:11:CC

---

### Finance Department (V-LAN 40)

**F1: Finance Head**

- **Email:** f1.head@corp.local
- **Hostname:** FIN-HEAD-L (Laptop)
- **MAC Address**: 00:E0:4C:4B:22:11
- Internal Office IP (VLAN 40): 10.40.1.10
- Home Router Public WAN IP: 203.0.113.50
- Remote Work VPN IP: 172.16.40.10

**F2: Accountant**

- **Email:** f2.accountant@corp.local
- **Hostname:** FIN-ACCT-L (Laptop)
- **MAC Address**: 00:E0:4C:4B:22:22
- Internal Office IP (VLAN 40): 10.40.1.20
- Home Router Public WAN IP: 198.51.100.72
- Remote Work VPN IP: 172.16.40.20


**F3: CFA Intern**

- **Email:** f3.intern@corp.local
- **Hostname:** FIN-INT-L (Laptop)
- **MAC Address**: 00:E0:4C:4B:22:33
- Internal Office IP (VLAN 40): 10.40.1.30
- Home Router Public WAN IP: 23.45.67.89
- Remote Work VPN IP: 172.16.40.30

---

### 🛠️ IT Department (VLAN 50 - Core Infrastructure Admins)

**IT1: IT Head**
- **Email:** it1.head@corp.local
- **Hostname:** IT-HEAD-D (Desktop)
- **Internal IP** (Office): 10.50.1.10
- **MAC Address**: 00:E0:4C:5C:33:AA

**IT2: Networking Guy**
- **Email:** it2.net@corp.local
- **Hostname:** IT-NET-D (Desktop)
- **Internal IP** (Office): 10.50.1.20
- **MAC Address**: 00:E0:4C:5C:33:BB

**IT3: IT Support Guy**
- **Email:** it3.support@corp.local
- **Hostname:** IT-SUP-D (Desktop)
- **Internal IP** (Office): 10.50.1.30
- **MAC Address**: 00:E0:4C:5C:33:CC

----

### 💻 Developers (VLAN 60 - Engineering & Dev Operations)

**D1: Developer Head**
- **Email:** d1.devhead@corp.local
- **Hostname:** DEV-HEAD-D
- **Internal IP** (Office): 10.60.1.10
- **MAC Address**: 00:E0:4C:6D:44:11

**D2: Senior Developer**
- **Email:** d2.srdev@corp.local
- **Hostname:** DEV-SR01-D
- **Internal IP** (Office): 10.60.1.20
- **MAC Address**: 00:E0:4C:6D:44:22

**D3: Developer Employee**
- **Email:** d3.developer@corp.local
- **Hostname:** DEV-EMP01-D
- **Internal IP** (Office): 10.60.1.30
- **MAC Address**: 00:E0:4C:6D:44:33

**D4: Intern**
- **Email:** d4.intern@corp.local
- **Hostname:** DEV-INT01-D
- ****Internal IP**** (Office): 10.60.1.40
- **MAC Address**: 00:E0:4C:6D:44:44

