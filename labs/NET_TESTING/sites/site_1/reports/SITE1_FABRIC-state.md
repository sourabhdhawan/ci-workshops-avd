# Validate State Report

**Table of Contents:**

- [Validate State Report](validate-state-report)
  - [Test Results Summary](#test-results-summary)
  - [Failed Test Results Summary](#failed-test-results-summary)
  - [All Test Results](#all-test-results)

## Test Results Summary

### Summary Totals

| Total Tests | Total Tests Passed | Total Tests Failed | Total Tests Skipped |
| ----------- | ------------------ | ------------------ | ------------------- |
| 392 | 340 | 20 | 32 |

### Summary Totals Device Under Test

| Device Under Test | Total Tests | Tests Passed | Tests Failed | Tests Skipped | Categories Failed | Categories Skipped |
| ------------------| ----------- | ------------ | ------------ | ------------- | ----------------- | ------------------ |
| s1-brdr1 | 52 | 41 | 7 | 4 | BGP, Connectivity, System | Hardware |
| s1-brdr2 | 52 | 47 | 1 | 4 | System | Hardware |
| s1-leaf1 | 53 | 48 | 1 | 4 | System | Hardware |
| s1-leaf2 | 53 | 48 | 1 | 4 | System | Hardware |
| s1-leaf3 | 53 | 48 | 1 | 4 | System | Hardware |
| s1-leaf4 | 53 | 48 | 1 | 4 | System | Hardware |
| s1-spine1 | 38 | 30 | 4 | 4 | BGP, Connectivity, System | Hardware |
| s1-spine2 | 38 | 30 | 4 | 4 | BGP, Connectivity, System | Hardware |

### Summary Totals Per Category

| Test Category | Total Tests | Tests Passed | Tests Failed | Tests Skipped |
| ------------- | ----------- | ------------ | ------------ | ------------- |
| BGP | 54 | 50 | 4 | 0 |
| Connectivity | 108 | 100 | 8 | 0 |
| Hardware | 32 | 0 | 0 | 32 |
| Interfaces | 102 | 102 | 0 | 0 |
| MLAG | 6 | 6 | 0 | 0 |
| Routing | 74 | 74 | 0 | 0 |
| System | 16 | 8 | 8 | 0 |

## Failed Test Results Summary

| ID | Device Under Test | Categories | Test | Description | Inputs | Result | Messages |
| -- | ----------------- | ---------- | ---- | ----------- | ------ | -------| -------- |
| 4 | s1-brdr1 | BGP | VerifyBGPSpecificPeers | Verifies the health of specific BGP peer(s) for given address families. | BGP IPv4 Unicast Peer: s1-spine1 (IP: 172.16.1.16) | FAIL | AFI: ipv4 SAFI: unicast VRF: default Peer: 172.16.1.16 - Session state is not established - State: Active |
| 5 | s1-brdr1 | BGP | VerifyBGPSpecificPeers | Verifies the health of specific BGP peer(s) for given address families. | BGP IPv4 Unicast Peer: s1-spine2 (IP: 172.16.1.18) | FAIL | AFI: ipv4 SAFI: unicast VRF: default Peer: 172.16.1.18 - Session state is not established - State: Active |
| 7 | s1-brdr1 | Connectivity | VerifyLLDPNeighbors | Verifies the connection status of the specified LLDP (Link Layer Discovery Protocol) neighbors. | Local: Ethernet2 - Remote: s1-spine1 Ethernet6 | FAIL | Port Ethernet2 (Neighbor: s1-spine1.atd.lab, Neighbor Port: Ethernet6) - Wrong LLDP neighbors: s1-spine1.atd.lab/Ethernet7 |
| 8 | s1-brdr1 | Connectivity | VerifyLLDPNeighbors | Verifies the connection status of the specified LLDP (Link Layer Discovery Protocol) neighbors. | Local: Ethernet3 - Remote: s1-spine2 Ethernet6 | FAIL | Port Ethernet3 (Neighbor: s1-spine2.atd.lab, Neighbor Port: Ethernet6) - Wrong LLDP neighbors: s1-spine2.atd.lab/Ethernet7 |
| 18 | s1-brdr1 | Connectivity | VerifyReachability | Test network reachability to one or many destination IP(s). | Source: P2P Interface Ethernet2 (IP: 172.16.1.17) - Destination: s1-spine1 Ethernet6 (IP: 172.16.1.16) | FAIL | Host 172.16.1.16 (src: 172.16.1.17, vrf: default, size: 100B, repeat: 1) - Unreachable |
| 19 | s1-brdr1 | Connectivity | VerifyReachability | Test network reachability to one or many destination IP(s). | Source: P2P Interface Ethernet3 (IP: 172.16.1.19) - Destination: s1-spine2 Ethernet6 (IP: 172.16.1.18) | FAIL | Host 172.16.1.18 (src: 172.16.1.19, vrf: default, size: 100B, repeat: 1) - Unreachable |
| 52 | s1-brdr1 | System | VerifyReloadCause | Verifies the last reload cause of the device. | - | FAIL | Reload cause is: 'System reloaded due to Zero Touch Provisioning' |
| 104 | s1-brdr2 | System | VerifyReloadCause | Verifies the last reload cause of the device. | - | FAIL | Reload cause is: 'System reloaded due to Zero Touch Provisioning' |
| 157 | s1-leaf1 | System | VerifyReloadCause | Verifies the last reload cause of the device. | - | FAIL | Reload cause is: 'System reloaded due to Zero Touch Provisioning' |
| 210 | s1-leaf2 | System | VerifyReloadCause | Verifies the last reload cause of the device. | - | FAIL | Reload cause is: 'System reloaded due to Zero Touch Provisioning' |
| 263 | s1-leaf3 | System | VerifyReloadCause | Verifies the last reload cause of the device. | - | FAIL | Reload cause is: 'System reloaded due to Zero Touch Provisioning' |
| 316 | s1-leaf4 | System | VerifyReloadCause | Verifies the last reload cause of the device. | - | FAIL | Reload cause is: 'System reloaded due to Zero Touch Provisioning' |
| 323 | s1-spine1 | BGP | VerifyBGPSpecificPeers | Verifies the health of specific BGP peer(s) for given address families. | BGP IPv4 Unicast Peer: s1-brdr1 (IP: 172.16.1.17) | FAIL | AFI: ipv4 SAFI: unicast VRF: default Peer: 172.16.1.17 - Session state is not established - State: Active |
| 333 | s1-spine1 | Connectivity | VerifyLLDPNeighbors | Verifies the connection status of the specified LLDP (Link Layer Discovery Protocol) neighbors. | Local: Ethernet6 - Remote: s1-brdr1 Ethernet2 | FAIL | Port Ethernet6 (Neighbor: s1-brdr1.atd.lab, Neighbor Port: Ethernet2) - Wrong LLDP neighbors: s1-spine2.atd.lab/Ethernet6 |
| 339 | s1-spine1 | Connectivity | VerifyReachability | Test network reachability to one or many destination IP(s). | Source: P2P Interface Ethernet6 (IP: 172.16.1.16) - Destination: s1-brdr1 Ethernet2 (IP: 172.16.1.17) | FAIL | Host 172.16.1.17 (src: 172.16.1.16, vrf: default, size: 100B, repeat: 1) - Unreachable |
| 354 | s1-spine1 | System | VerifyReloadCause | Verifies the last reload cause of the device. | - | FAIL | Reload cause is: 'System reloaded due to Zero Touch Provisioning' |
| 361 | s1-spine2 | BGP | VerifyBGPSpecificPeers | Verifies the health of specific BGP peer(s) for given address families. | BGP IPv4 Unicast Peer: s1-brdr1 (IP: 172.16.1.19) | FAIL | AFI: ipv4 SAFI: unicast VRF: default Peer: 172.16.1.19 - Session state is not established - State: Active |
| 371 | s1-spine2 | Connectivity | VerifyLLDPNeighbors | Verifies the connection status of the specified LLDP (Link Layer Discovery Protocol) neighbors. | Local: Ethernet6 - Remote: s1-brdr1 Ethernet3 | FAIL | Port Ethernet6 (Neighbor: s1-brdr1.atd.lab, Neighbor Port: Ethernet3) - Wrong LLDP neighbors: s1-spine1.atd.lab/Ethernet6 |
| 377 | s1-spine2 | Connectivity | VerifyReachability | Test network reachability to one or many destination IP(s). | Source: P2P Interface Ethernet6 (IP: 172.16.1.18) - Destination: s1-brdr1 Ethernet3 (IP: 172.16.1.19) | FAIL | Host 172.16.1.19 (src: 172.16.1.18, vrf: default, size: 100B, repeat: 1) - Unreachable |
| 392 | s1-spine2 | System | VerifyReloadCause | Verifies the last reload cause of the device. | - | FAIL | Reload cause is: 'System reloaded due to Zero Touch Provisioning' |

## All Test Results

| ID | Device Under Test | Categories | Test | Description | Inputs | Result | Messages |
| -- | ----------------- | ---------- | ---- | ----------- | ------ | -------| -------- |
| 1 | s1-brdr1 | BGP | VerifyBGPSpecificPeers | Verifies the health of specific BGP peer(s) for given address families. | BGP EVPN Peer: s1-spine1 (IP: 10.250.1.1) | PASS | - |
| 2 | s1-brdr1 | BGP | VerifyBGPSpecificPeers | Verifies the health of specific BGP peer(s) for given address families. | BGP EVPN Peer: s1-spine2 (IP: 10.250.1.2) | PASS | - |
| 3 | s1-brdr1 | BGP | VerifyBGPSpecificPeers | Verifies the health of specific BGP peer(s) for given address families. | BGP IPv4 Unicast Peer: s1-brdr2 (IP: 10.252.1.9) | PASS | - |
| 4 | s1-brdr1 | BGP | VerifyBGPSpecificPeers | Verifies the health of specific BGP peer(s) for given address families. | BGP IPv4 Unicast Peer: s1-spine1 (IP: 172.16.1.16) | FAIL | AFI: ipv4 SAFI: unicast VRF: default Peer: 172.16.1.16 - Session state is not established - State: Active |
| 5 | s1-brdr1 | BGP | VerifyBGPSpecificPeers | Verifies the health of specific BGP peer(s) for given address families. | BGP IPv4 Unicast Peer: s1-spine2 (IP: 172.16.1.18) | FAIL | AFI: ipv4 SAFI: unicast VRF: default Peer: 172.16.1.18 - Session state is not established - State: Active |
| 6 | s1-brdr1 | Connectivity | VerifyLLDPNeighbors | Verifies the connection status of the specified LLDP (Link Layer Discovery Protocol) neighbors. | Local: Ethernet1 - Remote: s1-brdr2 Ethernet1 | PASS | - |
| 7 | s1-brdr1 | Connectivity | VerifyLLDPNeighbors | Verifies the connection status of the specified LLDP (Link Layer Discovery Protocol) neighbors. | Local: Ethernet2 - Remote: s1-spine1 Ethernet6 | FAIL | Port Ethernet2 (Neighbor: s1-spine1.atd.lab, Neighbor Port: Ethernet6) - Wrong LLDP neighbors: s1-spine1.atd.lab/Ethernet7 |
| 8 | s1-brdr1 | Connectivity | VerifyLLDPNeighbors | Verifies the connection status of the specified LLDP (Link Layer Discovery Protocol) neighbors. | Local: Ethernet3 - Remote: s1-spine2 Ethernet6 | FAIL | Port Ethernet3 (Neighbor: s1-spine2.atd.lab, Neighbor Port: Ethernet6) - Wrong LLDP neighbors: s1-spine2.atd.lab/Ethernet7 |
| 9 | s1-brdr1 | Connectivity | VerifyLLDPNeighbors | Verifies the connection status of the specified LLDP (Link Layer Discovery Protocol) neighbors. | Local: Ethernet6 - Remote: s1-brdr2 Ethernet6 | PASS | - |
| 10 | s1-brdr1 | Connectivity | VerifyReachability | Test network reachability to one or many destination IP(s). | Source: Loopback0 (IP: 10.250.1.7) - Destination: s1-brdr1 Loopback0 (IP: 10.250.1.7) | PASS | - |
| 11 | s1-brdr1 | Connectivity | VerifyReachability | Test network reachability to one or many destination IP(s). | Source: Loopback0 (IP: 10.250.1.7) - Destination: s1-brdr2 Loopback0 (IP: 10.250.1.8) | PASS | - |
| 12 | s1-brdr1 | Connectivity | VerifyReachability | Test network reachability to one or many destination IP(s). | Source: Loopback0 (IP: 10.250.1.7) - Destination: s1-leaf1 Loopback0 (IP: 10.250.1.3) | PASS | - |
| 13 | s1-brdr1 | Connectivity | VerifyReachability | Test network reachability to one or many destination IP(s). | Source: Loopback0 (IP: 10.250.1.7) - Destination: s1-leaf2 Loopback0 (IP: 10.250.1.4) | PASS | - |
| 14 | s1-brdr1 | Connectivity | VerifyReachability | Test network reachability to one or many destination IP(s). | Source: Loopback0 (IP: 10.250.1.7) - Destination: s1-leaf3 Loopback0 (IP: 10.250.1.5) | PASS | - |
| 15 | s1-brdr1 | Connectivity | VerifyReachability | Test network reachability to one or many destination IP(s). | Source: Loopback0 (IP: 10.250.1.7) - Destination: s1-leaf4 Loopback0 (IP: 10.250.1.6) | PASS | - |
| 16 | s1-brdr1 | Connectivity | VerifyReachability | Test network reachability to one or many destination IP(s). | Source: Loopback0 (IP: 10.250.1.7) - Destination: s1-spine1 Loopback0 (IP: 10.250.1.1) | PASS | - |
| 17 | s1-brdr1 | Connectivity | VerifyReachability | Test network reachability to one or many destination IP(s). | Source: Loopback0 (IP: 10.250.1.7) - Destination: s1-spine2 Loopback0 (IP: 10.250.1.2) | PASS | - |
| 18 | s1-brdr1 | Connectivity | VerifyReachability | Test network reachability to one or many destination IP(s). | Source: P2P Interface Ethernet2 (IP: 172.16.1.17) - Destination: s1-spine1 Ethernet6 (IP: 172.16.1.16) | FAIL | Host 172.16.1.16 (src: 172.16.1.17, vrf: default, size: 100B, repeat: 1) - Unreachable |
| 19 | s1-brdr1 | Connectivity | VerifyReachability | Test network reachability to one or many destination IP(s). | Source: P2P Interface Ethernet3 (IP: 172.16.1.19) - Destination: s1-spine2 Ethernet6 (IP: 172.16.1.18) | FAIL | Host 172.16.1.18 (src: 172.16.1.19, vrf: default, size: 100B, repeat: 1) - Unreachable |
| 20 | s1-brdr1 | Hardware | VerifyEnvironmentCooling | Verifies the status of power supply fans and all fan trays. | Accepted States: 'ok' | SKIPPED | VerifyEnvironmentCooling test is not supported on cEOSLab. |
| 21 | s1-brdr1 | Hardware | VerifyEnvironmentPower | Verifies the power supplies status. | Accepted States: 'ok' | SKIPPED | VerifyEnvironmentPower test is not supported on cEOSLab. |
| 22 | s1-brdr1 | Hardware | VerifyTemperature | Verifies if the device temperature is within acceptable limits. | - | SKIPPED | VerifyTemperature test is not supported on cEOSLab. |
| 23 | s1-brdr1 | Hardware | VerifyTransceiversManufacturers | Verifies if all the transceivers come from approved manufacturers. | Accepted Manufacturers: 'Arista Networks', 'Arastra, Inc.', 'Not Present' | SKIPPED | VerifyTransceiversManufacturers test is not supported on cEOSLab. |
| 24 | s1-brdr1 | Interfaces | VerifyInterfacesStatus | Verifies the operational states of specified interfaces to ensure they match expected configurations. | Interface Ethernet1 - MLAG_s1-brdr2_Ethernet1 = 'up' | PASS | - |
| 25 | s1-brdr1 | Interfaces | VerifyInterfacesStatus | Verifies the operational states of specified interfaces to ensure they match expected configurations. | Interface Ethernet2 - P2P_s1-spine1_Ethernet6 = 'up' | PASS | - |
| 26 | s1-brdr1 | Interfaces | VerifyInterfacesStatus | Verifies the operational states of specified interfaces to ensure they match expected configurations. | Interface Ethernet3 - P2P_s1-spine2_Ethernet6 = 'up' | PASS | - |
| 27 | s1-brdr1 | Interfaces | VerifyInterfacesStatus | Verifies the operational states of specified interfaces to ensure they match expected configurations. | Interface Ethernet4 - P2P_s2-brdr1_Ethernet4 = 'up' | PASS | - |
| 28 | s1-brdr1 | Interfaces | VerifyInterfacesStatus | Verifies the operational states of specified interfaces to ensure they match expected configurations. | Interface Ethernet6 - MLAG_s1-brdr2_Ethernet6 = 'up' | PASS | - |
| 29 | s1-brdr1 | Interfaces | VerifyInterfacesStatus | Verifies the operational states of specified interfaces to ensure they match expected configurations. | Interface Loopback0 - ROUTER_ID = 'up' | PASS | - |
| 30 | s1-brdr1 | Interfaces | VerifyInterfacesStatus | Verifies the operational states of specified interfaces to ensure they match expected configurations. | Interface Loopback1 - VXLAN_TUNNEL_SOURCE = 'up' | PASS | - |
| 31 | s1-brdr1 | Interfaces | VerifyInterfacesStatus | Verifies the operational states of specified interfaces to ensure they match expected configurations. | Interface Port-Channel1 - MLAG_s1-brdr2_Port-Channel1 = 'up' | PASS | - |
| 32 | s1-brdr1 | Interfaces | VerifyInterfacesStatus | Verifies the operational states of specified interfaces to ensure they match expected configurations. | Interface Vlan10 - Ten = 'up' | PASS | - |
| 33 | s1-brdr1 | Interfaces | VerifyInterfacesStatus | Verifies the operational states of specified interfaces to ensure they match expected configurations. | Interface Vlan20 - Twenty = 'up' | PASS | - |
| 34 | s1-brdr1 | Interfaces | VerifyInterfacesStatus | Verifies the operational states of specified interfaces to ensure they match expected configurations. | Interface Vlan3009 - MLAG_L3_VRF_OVERLAY = 'up' | PASS | - |
| 35 | s1-brdr1 | Interfaces | VerifyInterfacesStatus | Verifies the operational states of specified interfaces to ensure they match expected configurations. | Interface Vlan4093 - MLAG_L3 = 'up' | PASS | - |
| 36 | s1-brdr1 | Interfaces | VerifyInterfacesStatus | Verifies the operational states of specified interfaces to ensure they match expected configurations. | Interface Vlan4094 - MLAG = 'up' | PASS | - |
| 37 | s1-brdr1 | Interfaces | VerifyInterfacesStatus | Verifies the operational states of specified interfaces to ensure they match expected configurations. | Interface Vxlan1 = 'up' | PASS | - |
| 38 | s1-brdr1 | MLAG | VerifyMlagStatus | Verifies the health status of the MLAG configuration. | - | PASS | - |
| 39 | s1-brdr1 | Routing | VerifyRoutingProtocolModel | Verifies the configured routing protocol model. | Routing protocol model: multi-agent | PASS | - |
| 40 | s1-brdr1 | Routing | VerifyRoutingTableEntry | Verifies that the provided routes are present in the routing table of a specified VRF. | Route: 10.250.1.1 - Peer: s1-spine1 | PASS | - |
| 41 | s1-brdr1 | Routing | VerifyRoutingTableEntry | Verifies that the provided routes are present in the routing table of a specified VRF. | Route: 10.250.1.2 - Peer: s1-spine2 | PASS | - |
| 42 | s1-brdr1 | Routing | VerifyRoutingTableEntry | Verifies that the provided routes are present in the routing table of a specified VRF. | Route: 10.250.1.3 - Peer: s1-leaf1 | PASS | - |
| 43 | s1-brdr1 | Routing | VerifyRoutingTableEntry | Verifies that the provided routes are present in the routing table of a specified VRF. | Route: 10.250.1.4 - Peer: s1-leaf2 | PASS | - |
| 44 | s1-brdr1 | Routing | VerifyRoutingTableEntry | Verifies that the provided routes are present in the routing table of a specified VRF. | Route: 10.250.1.5 - Peer: s1-leaf3 | PASS | - |
| 45 | s1-brdr1 | Routing | VerifyRoutingTableEntry | Verifies that the provided routes are present in the routing table of a specified VRF. | Route: 10.250.1.6 - Peer: s1-leaf4 | PASS | - |
| 46 | s1-brdr1 | Routing | VerifyRoutingTableEntry | Verifies that the provided routes are present in the routing table of a specified VRF. | Route: 10.250.1.7 - Peer: s1-brdr1 | PASS | - |
| 47 | s1-brdr1 | Routing | VerifyRoutingTableEntry | Verifies that the provided routes are present in the routing table of a specified VRF. | Route: 10.250.1.8 - Peer: s1-brdr2 | PASS | - |
| 48 | s1-brdr1 | Routing | VerifyRoutingTableEntry | Verifies that the provided routes are present in the routing table of a specified VRF. | Route: 10.255.1.3 - Peer: s1-leaf1 | PASS | - |
| 49 | s1-brdr1 | Routing | VerifyRoutingTableEntry | Verifies that the provided routes are present in the routing table of a specified VRF. | Route: 10.255.1.5 - Peer: s1-leaf3 | PASS | - |
| 50 | s1-brdr1 | Routing | VerifyRoutingTableEntry | Verifies that the provided routes are present in the routing table of a specified VRF. | Route: 10.255.1.7 - Peer: s1-brdr1 | PASS | - |
| 51 | s1-brdr1 | System | VerifyNTP | Verifies if NTP is synchronised. | - | PASS | - |
| 52 | s1-brdr1 | System | VerifyReloadCause | Verifies the last reload cause of the device. | - | FAIL | Reload cause is: 'System reloaded due to Zero Touch Provisioning' |
| 53 | s1-brdr2 | BGP | VerifyBGPSpecificPeers | Verifies the health of specific BGP peer(s) for given address families. | BGP EVPN Peer: s1-spine1 (IP: 10.250.1.1) | PASS | - |
| 54 | s1-brdr2 | BGP | VerifyBGPSpecificPeers | Verifies the health of specific BGP peer(s) for given address families. | BGP EVPN Peer: s1-spine2 (IP: 10.250.1.2) | PASS | - |
| 55 | s1-brdr2 | BGP | VerifyBGPSpecificPeers | Verifies the health of specific BGP peer(s) for given address families. | BGP IPv4 Unicast Peer: s1-brdr1 (IP: 10.252.1.8) | PASS | - |
| 56 | s1-brdr2 | BGP | VerifyBGPSpecificPeers | Verifies the health of specific BGP peer(s) for given address families. | BGP IPv4 Unicast Peer: s1-spine1 (IP: 172.16.1.20) | PASS | - |
| 57 | s1-brdr2 | BGP | VerifyBGPSpecificPeers | Verifies the health of specific BGP peer(s) for given address families. | BGP IPv4 Unicast Peer: s1-spine2 (IP: 172.16.1.22) | PASS | - |
| 58 | s1-brdr2 | Connectivity | VerifyLLDPNeighbors | Verifies the connection status of the specified LLDP (Link Layer Discovery Protocol) neighbors. | Local: Ethernet1 - Remote: s1-brdr1 Ethernet1 | PASS | - |
| 59 | s1-brdr2 | Connectivity | VerifyLLDPNeighbors | Verifies the connection status of the specified LLDP (Link Layer Discovery Protocol) neighbors. | Local: Ethernet2 - Remote: s1-spine1 Ethernet8 | PASS | - |
| 60 | s1-brdr2 | Connectivity | VerifyLLDPNeighbors | Verifies the connection status of the specified LLDP (Link Layer Discovery Protocol) neighbors. | Local: Ethernet3 - Remote: s1-spine2 Ethernet8 | PASS | - |
| 61 | s1-brdr2 | Connectivity | VerifyLLDPNeighbors | Verifies the connection status of the specified LLDP (Link Layer Discovery Protocol) neighbors. | Local: Ethernet6 - Remote: s1-brdr1 Ethernet6 | PASS | - |
| 62 | s1-brdr2 | Connectivity | VerifyReachability | Test network reachability to one or many destination IP(s). | Source: Loopback0 (IP: 10.250.1.8) - Destination: s1-brdr1 Loopback0 (IP: 10.250.1.7) | PASS | - |
| 63 | s1-brdr2 | Connectivity | VerifyReachability | Test network reachability to one or many destination IP(s). | Source: Loopback0 (IP: 10.250.1.8) - Destination: s1-brdr2 Loopback0 (IP: 10.250.1.8) | PASS | - |
| 64 | s1-brdr2 | Connectivity | VerifyReachability | Test network reachability to one or many destination IP(s). | Source: Loopback0 (IP: 10.250.1.8) - Destination: s1-leaf1 Loopback0 (IP: 10.250.1.3) | PASS | - |
| 65 | s1-brdr2 | Connectivity | VerifyReachability | Test network reachability to one or many destination IP(s). | Source: Loopback0 (IP: 10.250.1.8) - Destination: s1-leaf2 Loopback0 (IP: 10.250.1.4) | PASS | - |
| 66 | s1-brdr2 | Connectivity | VerifyReachability | Test network reachability to one or many destination IP(s). | Source: Loopback0 (IP: 10.250.1.8) - Destination: s1-leaf3 Loopback0 (IP: 10.250.1.5) | PASS | - |
| 67 | s1-brdr2 | Connectivity | VerifyReachability | Test network reachability to one or many destination IP(s). | Source: Loopback0 (IP: 10.250.1.8) - Destination: s1-leaf4 Loopback0 (IP: 10.250.1.6) | PASS | - |
| 68 | s1-brdr2 | Connectivity | VerifyReachability | Test network reachability to one or many destination IP(s). | Source: Loopback0 (IP: 10.250.1.8) - Destination: s1-spine1 Loopback0 (IP: 10.250.1.1) | PASS | - |
| 69 | s1-brdr2 | Connectivity | VerifyReachability | Test network reachability to one or many destination IP(s). | Source: Loopback0 (IP: 10.250.1.8) - Destination: s1-spine2 Loopback0 (IP: 10.250.1.2) | PASS | - |
| 70 | s1-brdr2 | Connectivity | VerifyReachability | Test network reachability to one or many destination IP(s). | Source: P2P Interface Ethernet2 (IP: 172.16.1.21) - Destination: s1-spine1 Ethernet8 (IP: 172.16.1.20) | PASS | - |
| 71 | s1-brdr2 | Connectivity | VerifyReachability | Test network reachability to one or many destination IP(s). | Source: P2P Interface Ethernet3 (IP: 172.16.1.23) - Destination: s1-spine2 Ethernet8 (IP: 172.16.1.22) | PASS | - |
| 72 | s1-brdr2 | Hardware | VerifyEnvironmentCooling | Verifies the status of power supply fans and all fan trays. | Accepted States: 'ok' | SKIPPED | VerifyEnvironmentCooling test is not supported on cEOSLab. |
| 73 | s1-brdr2 | Hardware | VerifyEnvironmentPower | Verifies the power supplies status. | Accepted States: 'ok' | SKIPPED | VerifyEnvironmentPower test is not supported on cEOSLab. |
| 74 | s1-brdr2 | Hardware | VerifyTemperature | Verifies if the device temperature is within acceptable limits. | - | SKIPPED | VerifyTemperature test is not supported on cEOSLab. |
| 75 | s1-brdr2 | Hardware | VerifyTransceiversManufacturers | Verifies if all the transceivers come from approved manufacturers. | Accepted Manufacturers: 'Arista Networks', 'Arastra, Inc.', 'Not Present' | SKIPPED | VerifyTransceiversManufacturers test is not supported on cEOSLab. |
| 76 | s1-brdr2 | Interfaces | VerifyInterfacesStatus | Verifies the operational states of specified interfaces to ensure they match expected configurations. | Interface Ethernet1 - MLAG_s1-brdr1_Ethernet1 = 'up' | PASS | - |
| 77 | s1-brdr2 | Interfaces | VerifyInterfacesStatus | Verifies the operational states of specified interfaces to ensure they match expected configurations. | Interface Ethernet2 - P2P_s1-spine1_Ethernet8 = 'up' | PASS | - |
| 78 | s1-brdr2 | Interfaces | VerifyInterfacesStatus | Verifies the operational states of specified interfaces to ensure they match expected configurations. | Interface Ethernet3 - P2P_s1-spine2_Ethernet8 = 'up' | PASS | - |
| 79 | s1-brdr2 | Interfaces | VerifyInterfacesStatus | Verifies the operational states of specified interfaces to ensure they match expected configurations. | Interface Ethernet5 - P2P_s2-brdr2_Ethernet5 = 'up' | PASS | - |
| 80 | s1-brdr2 | Interfaces | VerifyInterfacesStatus | Verifies the operational states of specified interfaces to ensure they match expected configurations. | Interface Ethernet6 - MLAG_s1-brdr1_Ethernet6 = 'up' | PASS | - |
| 81 | s1-brdr2 | Interfaces | VerifyInterfacesStatus | Verifies the operational states of specified interfaces to ensure they match expected configurations. | Interface Loopback0 - ROUTER_ID = 'up' | PASS | - |
| 82 | s1-brdr2 | Interfaces | VerifyInterfacesStatus | Verifies the operational states of specified interfaces to ensure they match expected configurations. | Interface Loopback1 - VXLAN_TUNNEL_SOURCE = 'up' | PASS | - |
| 83 | s1-brdr2 | Interfaces | VerifyInterfacesStatus | Verifies the operational states of specified interfaces to ensure they match expected configurations. | Interface Port-Channel1 - MLAG_s1-brdr1_Port-Channel1 = 'up' | PASS | - |
| 84 | s1-brdr2 | Interfaces | VerifyInterfacesStatus | Verifies the operational states of specified interfaces to ensure they match expected configurations. | Interface Vlan10 - Ten = 'up' | PASS | - |
| 85 | s1-brdr2 | Interfaces | VerifyInterfacesStatus | Verifies the operational states of specified interfaces to ensure they match expected configurations. | Interface Vlan20 - Twenty = 'up' | PASS | - |
| 86 | s1-brdr2 | Interfaces | VerifyInterfacesStatus | Verifies the operational states of specified interfaces to ensure they match expected configurations. | Interface Vlan3009 - MLAG_L3_VRF_OVERLAY = 'up' | PASS | - |
| 87 | s1-brdr2 | Interfaces | VerifyInterfacesStatus | Verifies the operational states of specified interfaces to ensure they match expected configurations. | Interface Vlan4093 - MLAG_L3 = 'up' | PASS | - |
| 88 | s1-brdr2 | Interfaces | VerifyInterfacesStatus | Verifies the operational states of specified interfaces to ensure they match expected configurations. | Interface Vlan4094 - MLAG = 'up' | PASS | - |
| 89 | s1-brdr2 | Interfaces | VerifyInterfacesStatus | Verifies the operational states of specified interfaces to ensure they match expected configurations. | Interface Vxlan1 = 'up' | PASS | - |
| 90 | s1-brdr2 | MLAG | VerifyMlagStatus | Verifies the health status of the MLAG configuration. | - | PASS | - |
| 91 | s1-brdr2 | Routing | VerifyRoutingProtocolModel | Verifies the configured routing protocol model. | Routing protocol model: multi-agent | PASS | - |
| 92 | s1-brdr2 | Routing | VerifyRoutingTableEntry | Verifies that the provided routes are present in the routing table of a specified VRF. | Route: 10.250.1.1 - Peer: s1-spine1 | PASS | - |
| 93 | s1-brdr2 | Routing | VerifyRoutingTableEntry | Verifies that the provided routes are present in the routing table of a specified VRF. | Route: 10.250.1.2 - Peer: s1-spine2 | PASS | - |
| 94 | s1-brdr2 | Routing | VerifyRoutingTableEntry | Verifies that the provided routes are present in the routing table of a specified VRF. | Route: 10.250.1.3 - Peer: s1-leaf1 | PASS | - |
| 95 | s1-brdr2 | Routing | VerifyRoutingTableEntry | Verifies that the provided routes are present in the routing table of a specified VRF. | Route: 10.250.1.4 - Peer: s1-leaf2 | PASS | - |
| 96 | s1-brdr2 | Routing | VerifyRoutingTableEntry | Verifies that the provided routes are present in the routing table of a specified VRF. | Route: 10.250.1.5 - Peer: s1-leaf3 | PASS | - |
| 97 | s1-brdr2 | Routing | VerifyRoutingTableEntry | Verifies that the provided routes are present in the routing table of a specified VRF. | Route: 10.250.1.6 - Peer: s1-leaf4 | PASS | - |
| 98 | s1-brdr2 | Routing | VerifyRoutingTableEntry | Verifies that the provided routes are present in the routing table of a specified VRF. | Route: 10.250.1.7 - Peer: s1-brdr1 | PASS | - |
| 99 | s1-brdr2 | Routing | VerifyRoutingTableEntry | Verifies that the provided routes are present in the routing table of a specified VRF. | Route: 10.250.1.8 - Peer: s1-brdr2 | PASS | - |
| 100 | s1-brdr2 | Routing | VerifyRoutingTableEntry | Verifies that the provided routes are present in the routing table of a specified VRF. | Route: 10.255.1.3 - Peer: s1-leaf1 | PASS | - |
| 101 | s1-brdr2 | Routing | VerifyRoutingTableEntry | Verifies that the provided routes are present in the routing table of a specified VRF. | Route: 10.255.1.5 - Peer: s1-leaf3 | PASS | - |
| 102 | s1-brdr2 | Routing | VerifyRoutingTableEntry | Verifies that the provided routes are present in the routing table of a specified VRF. | Route: 10.255.1.7 - Peer: s1-brdr1 | PASS | - |
| 103 | s1-brdr2 | System | VerifyNTP | Verifies if NTP is synchronised. | - | PASS | - |
| 104 | s1-brdr2 | System | VerifyReloadCause | Verifies the last reload cause of the device. | - | FAIL | Reload cause is: 'System reloaded due to Zero Touch Provisioning' |
| 105 | s1-leaf1 | BGP | VerifyBGPSpecificPeers | Verifies the health of specific BGP peer(s) for given address families. | BGP EVPN Peer: s1-spine1 (IP: 10.250.1.1) | PASS | - |
| 106 | s1-leaf1 | BGP | VerifyBGPSpecificPeers | Verifies the health of specific BGP peer(s) for given address families. | BGP EVPN Peer: s1-spine2 (IP: 10.250.1.2) | PASS | - |
| 107 | s1-leaf1 | BGP | VerifyBGPSpecificPeers | Verifies the health of specific BGP peer(s) for given address families. | BGP IPv4 Unicast Peer: s1-leaf2 (IP: 10.252.1.1) | PASS | - |
| 108 | s1-leaf1 | BGP | VerifyBGPSpecificPeers | Verifies the health of specific BGP peer(s) for given address families. | BGP IPv4 Unicast Peer: s1-spine1 (IP: 172.16.1.0) | PASS | - |
| 109 | s1-leaf1 | BGP | VerifyBGPSpecificPeers | Verifies the health of specific BGP peer(s) for given address families. | BGP IPv4 Unicast Peer: s1-spine2 (IP: 172.16.1.2) | PASS | - |
| 110 | s1-leaf1 | Connectivity | VerifyLLDPNeighbors | Verifies the connection status of the specified LLDP (Link Layer Discovery Protocol) neighbors. | Local: Ethernet1 - Remote: s1-leaf2 Ethernet1 | PASS | - |
| 111 | s1-leaf1 | Connectivity | VerifyLLDPNeighbors | Verifies the connection status of the specified LLDP (Link Layer Discovery Protocol) neighbors. | Local: Ethernet2 - Remote: s1-spine1 Ethernet2 | PASS | - |
| 112 | s1-leaf1 | Connectivity | VerifyLLDPNeighbors | Verifies the connection status of the specified LLDP (Link Layer Discovery Protocol) neighbors. | Local: Ethernet3 - Remote: s1-spine2 Ethernet2 | PASS | - |
| 113 | s1-leaf1 | Connectivity | VerifyLLDPNeighbors | Verifies the connection status of the specified LLDP (Link Layer Discovery Protocol) neighbors. | Local: Ethernet6 - Remote: s1-leaf2 Ethernet6 | PASS | - |
| 114 | s1-leaf1 | Connectivity | VerifyReachability | Test network reachability to one or many destination IP(s). | Source: Loopback0 (IP: 10.250.1.3) - Destination: s1-brdr1 Loopback0 (IP: 10.250.1.7) | PASS | - |
| 115 | s1-leaf1 | Connectivity | VerifyReachability | Test network reachability to one or many destination IP(s). | Source: Loopback0 (IP: 10.250.1.3) - Destination: s1-brdr2 Loopback0 (IP: 10.250.1.8) | PASS | - |
| 116 | s1-leaf1 | Connectivity | VerifyReachability | Test network reachability to one or many destination IP(s). | Source: Loopback0 (IP: 10.250.1.3) - Destination: s1-leaf1 Loopback0 (IP: 10.250.1.3) | PASS | - |
| 117 | s1-leaf1 | Connectivity | VerifyReachability | Test network reachability to one or many destination IP(s). | Source: Loopback0 (IP: 10.250.1.3) - Destination: s1-leaf2 Loopback0 (IP: 10.250.1.4) | PASS | - |
| 118 | s1-leaf1 | Connectivity | VerifyReachability | Test network reachability to one or many destination IP(s). | Source: Loopback0 (IP: 10.250.1.3) - Destination: s1-leaf3 Loopback0 (IP: 10.250.1.5) | PASS | - |
| 119 | s1-leaf1 | Connectivity | VerifyReachability | Test network reachability to one or many destination IP(s). | Source: Loopback0 (IP: 10.250.1.3) - Destination: s1-leaf4 Loopback0 (IP: 10.250.1.6) | PASS | - |
| 120 | s1-leaf1 | Connectivity | VerifyReachability | Test network reachability to one or many destination IP(s). | Source: Loopback0 (IP: 10.250.1.3) - Destination: s1-spine1 Loopback0 (IP: 10.250.1.1) | PASS | - |
| 121 | s1-leaf1 | Connectivity | VerifyReachability | Test network reachability to one or many destination IP(s). | Source: Loopback0 (IP: 10.250.1.3) - Destination: s1-spine2 Loopback0 (IP: 10.250.1.2) | PASS | - |
| 122 | s1-leaf1 | Connectivity | VerifyReachability | Test network reachability to one or many destination IP(s). | Source: P2P Interface Ethernet2 (IP: 172.16.1.1) - Destination: s1-spine1 Ethernet2 (IP: 172.16.1.0) | PASS | - |
| 123 | s1-leaf1 | Connectivity | VerifyReachability | Test network reachability to one or many destination IP(s). | Source: P2P Interface Ethernet3 (IP: 172.16.1.3) - Destination: s1-spine2 Ethernet2 (IP: 172.16.1.2) | PASS | - |
| 124 | s1-leaf1 | Hardware | VerifyEnvironmentCooling | Verifies the status of power supply fans and all fan trays. | Accepted States: 'ok' | SKIPPED | VerifyEnvironmentCooling test is not supported on cEOSLab. |
| 125 | s1-leaf1 | Hardware | VerifyEnvironmentPower | Verifies the power supplies status. | Accepted States: 'ok' | SKIPPED | VerifyEnvironmentPower test is not supported on cEOSLab. |
| 126 | s1-leaf1 | Hardware | VerifyTemperature | Verifies if the device temperature is within acceptable limits. | - | SKIPPED | VerifyTemperature test is not supported on cEOSLab. |
| 127 | s1-leaf1 | Hardware | VerifyTransceiversManufacturers | Verifies if all the transceivers come from approved manufacturers. | Accepted Manufacturers: 'Arista Networks', 'Arastra, Inc.', 'Not Present' | SKIPPED | VerifyTransceiversManufacturers test is not supported on cEOSLab. |
| 128 | s1-leaf1 | Interfaces | VerifyInterfacesStatus | Verifies the operational states of specified interfaces to ensure they match expected configurations. | Interface Ethernet1 - MLAG_s1-leaf2_Ethernet1 = 'up' | PASS | - |
| 129 | s1-leaf1 | Interfaces | VerifyInterfacesStatus | Verifies the operational states of specified interfaces to ensure they match expected configurations. | Interface Ethernet2 - P2P_s1-spine1_Ethernet2 = 'up' | PASS | - |
| 130 | s1-leaf1 | Interfaces | VerifyInterfacesStatus | Verifies the operational states of specified interfaces to ensure they match expected configurations. | Interface Ethernet3 - P2P_s1-spine2_Ethernet2 = 'up' | PASS | - |
| 131 | s1-leaf1 | Interfaces | VerifyInterfacesStatus | Verifies the operational states of specified interfaces to ensure they match expected configurations. | Interface Ethernet4 - SERVER_s1-host1_eth1 = 'up' | PASS | - |
| 132 | s1-leaf1 | Interfaces | VerifyInterfacesStatus | Verifies the operational states of specified interfaces to ensure they match expected configurations. | Interface Ethernet6 - MLAG_s1-leaf2_Ethernet6 = 'up' | PASS | - |
| 133 | s1-leaf1 | Interfaces | VerifyInterfacesStatus | Verifies the operational states of specified interfaces to ensure they match expected configurations. | Interface Loopback0 - ROUTER_ID = 'up' | PASS | - |
| 134 | s1-leaf1 | Interfaces | VerifyInterfacesStatus | Verifies the operational states of specified interfaces to ensure they match expected configurations. | Interface Loopback1 - VXLAN_TUNNEL_SOURCE = 'up' | PASS | - |
| 135 | s1-leaf1 | Interfaces | VerifyInterfacesStatus | Verifies the operational states of specified interfaces to ensure they match expected configurations. | Interface Port-Channel1 - MLAG_s1-leaf2_Port-Channel1 = 'up' | PASS | - |
| 136 | s1-leaf1 | Interfaces | VerifyInterfacesStatus | Verifies the operational states of specified interfaces to ensure they match expected configurations. | Interface Port-Channel4 - SERVER_s1-host1 = 'up' | PASS | - |
| 137 | s1-leaf1 | Interfaces | VerifyInterfacesStatus | Verifies the operational states of specified interfaces to ensure they match expected configurations. | Interface Vlan10 - Ten = 'up' | PASS | - |
| 138 | s1-leaf1 | Interfaces | VerifyInterfacesStatus | Verifies the operational states of specified interfaces to ensure they match expected configurations. | Interface Vlan20 - Twenty = 'up' | PASS | - |
| 139 | s1-leaf1 | Interfaces | VerifyInterfacesStatus | Verifies the operational states of specified interfaces to ensure they match expected configurations. | Interface Vlan3009 - MLAG_L3_VRF_OVERLAY = 'up' | PASS | - |
| 140 | s1-leaf1 | Interfaces | VerifyInterfacesStatus | Verifies the operational states of specified interfaces to ensure they match expected configurations. | Interface Vlan4093 - MLAG_L3 = 'up' | PASS | - |
| 141 | s1-leaf1 | Interfaces | VerifyInterfacesStatus | Verifies the operational states of specified interfaces to ensure they match expected configurations. | Interface Vlan4094 - MLAG = 'up' | PASS | - |
| 142 | s1-leaf1 | Interfaces | VerifyInterfacesStatus | Verifies the operational states of specified interfaces to ensure they match expected configurations. | Interface Vxlan1 = 'up' | PASS | - |
| 143 | s1-leaf1 | MLAG | VerifyMlagStatus | Verifies the health status of the MLAG configuration. | - | PASS | - |
| 144 | s1-leaf1 | Routing | VerifyRoutingProtocolModel | Verifies the configured routing protocol model. | Routing protocol model: multi-agent | PASS | - |
| 145 | s1-leaf1 | Routing | VerifyRoutingTableEntry | Verifies that the provided routes are present in the routing table of a specified VRF. | Route: 10.250.1.1 - Peer: s1-spine1 | PASS | - |
| 146 | s1-leaf1 | Routing | VerifyRoutingTableEntry | Verifies that the provided routes are present in the routing table of a specified VRF. | Route: 10.250.1.2 - Peer: s1-spine2 | PASS | - |
| 147 | s1-leaf1 | Routing | VerifyRoutingTableEntry | Verifies that the provided routes are present in the routing table of a specified VRF. | Route: 10.250.1.3 - Peer: s1-leaf1 | PASS | - |
| 148 | s1-leaf1 | Routing | VerifyRoutingTableEntry | Verifies that the provided routes are present in the routing table of a specified VRF. | Route: 10.250.1.4 - Peer: s1-leaf2 | PASS | - |
| 149 | s1-leaf1 | Routing | VerifyRoutingTableEntry | Verifies that the provided routes are present in the routing table of a specified VRF. | Route: 10.250.1.5 - Peer: s1-leaf3 | PASS | - |
| 150 | s1-leaf1 | Routing | VerifyRoutingTableEntry | Verifies that the provided routes are present in the routing table of a specified VRF. | Route: 10.250.1.6 - Peer: s1-leaf4 | PASS | - |
| 151 | s1-leaf1 | Routing | VerifyRoutingTableEntry | Verifies that the provided routes are present in the routing table of a specified VRF. | Route: 10.250.1.7 - Peer: s1-brdr1 | PASS | - |
| 152 | s1-leaf1 | Routing | VerifyRoutingTableEntry | Verifies that the provided routes are present in the routing table of a specified VRF. | Route: 10.250.1.8 - Peer: s1-brdr2 | PASS | - |
| 153 | s1-leaf1 | Routing | VerifyRoutingTableEntry | Verifies that the provided routes are present in the routing table of a specified VRF. | Route: 10.255.1.3 - Peer: s1-leaf1 | PASS | - |
| 154 | s1-leaf1 | Routing | VerifyRoutingTableEntry | Verifies that the provided routes are present in the routing table of a specified VRF. | Route: 10.255.1.5 - Peer: s1-leaf3 | PASS | - |
| 155 | s1-leaf1 | Routing | VerifyRoutingTableEntry | Verifies that the provided routes are present in the routing table of a specified VRF. | Route: 10.255.1.7 - Peer: s1-brdr1 | PASS | - |
| 156 | s1-leaf1 | System | VerifyNTP | Verifies if NTP is synchronised. | - | PASS | - |
| 157 | s1-leaf1 | System | VerifyReloadCause | Verifies the last reload cause of the device. | - | FAIL | Reload cause is: 'System reloaded due to Zero Touch Provisioning' |
| 158 | s1-leaf2 | BGP | VerifyBGPSpecificPeers | Verifies the health of specific BGP peer(s) for given address families. | BGP EVPN Peer: s1-spine1 (IP: 10.250.1.1) | PASS | - |
| 159 | s1-leaf2 | BGP | VerifyBGPSpecificPeers | Verifies the health of specific BGP peer(s) for given address families. | BGP EVPN Peer: s1-spine2 (IP: 10.250.1.2) | PASS | - |
| 160 | s1-leaf2 | BGP | VerifyBGPSpecificPeers | Verifies the health of specific BGP peer(s) for given address families. | BGP IPv4 Unicast Peer: s1-leaf1 (IP: 10.252.1.0) | PASS | - |
| 161 | s1-leaf2 | BGP | VerifyBGPSpecificPeers | Verifies the health of specific BGP peer(s) for given address families. | BGP IPv4 Unicast Peer: s1-spine1 (IP: 172.16.1.4) | PASS | - |
| 162 | s1-leaf2 | BGP | VerifyBGPSpecificPeers | Verifies the health of specific BGP peer(s) for given address families. | BGP IPv4 Unicast Peer: s1-spine2 (IP: 172.16.1.6) | PASS | - |
| 163 | s1-leaf2 | Connectivity | VerifyLLDPNeighbors | Verifies the connection status of the specified LLDP (Link Layer Discovery Protocol) neighbors. | Local: Ethernet1 - Remote: s1-leaf1 Ethernet1 | PASS | - |
| 164 | s1-leaf2 | Connectivity | VerifyLLDPNeighbors | Verifies the connection status of the specified LLDP (Link Layer Discovery Protocol) neighbors. | Local: Ethernet2 - Remote: s1-spine1 Ethernet3 | PASS | - |
| 165 | s1-leaf2 | Connectivity | VerifyLLDPNeighbors | Verifies the connection status of the specified LLDP (Link Layer Discovery Protocol) neighbors. | Local: Ethernet3 - Remote: s1-spine2 Ethernet3 | PASS | - |
| 166 | s1-leaf2 | Connectivity | VerifyLLDPNeighbors | Verifies the connection status of the specified LLDP (Link Layer Discovery Protocol) neighbors. | Local: Ethernet6 - Remote: s1-leaf1 Ethernet6 | PASS | - |
| 167 | s1-leaf2 | Connectivity | VerifyReachability | Test network reachability to one or many destination IP(s). | Source: Loopback0 (IP: 10.250.1.4) - Destination: s1-brdr1 Loopback0 (IP: 10.250.1.7) | PASS | - |
| 168 | s1-leaf2 | Connectivity | VerifyReachability | Test network reachability to one or many destination IP(s). | Source: Loopback0 (IP: 10.250.1.4) - Destination: s1-brdr2 Loopback0 (IP: 10.250.1.8) | PASS | - |
| 169 | s1-leaf2 | Connectivity | VerifyReachability | Test network reachability to one or many destination IP(s). | Source: Loopback0 (IP: 10.250.1.4) - Destination: s1-leaf1 Loopback0 (IP: 10.250.1.3) | PASS | - |
| 170 | s1-leaf2 | Connectivity | VerifyReachability | Test network reachability to one or many destination IP(s). | Source: Loopback0 (IP: 10.250.1.4) - Destination: s1-leaf2 Loopback0 (IP: 10.250.1.4) | PASS | - |
| 171 | s1-leaf2 | Connectivity | VerifyReachability | Test network reachability to one or many destination IP(s). | Source: Loopback0 (IP: 10.250.1.4) - Destination: s1-leaf3 Loopback0 (IP: 10.250.1.5) | PASS | - |
| 172 | s1-leaf2 | Connectivity | VerifyReachability | Test network reachability to one or many destination IP(s). | Source: Loopback0 (IP: 10.250.1.4) - Destination: s1-leaf4 Loopback0 (IP: 10.250.1.6) | PASS | - |
| 173 | s1-leaf2 | Connectivity | VerifyReachability | Test network reachability to one or many destination IP(s). | Source: Loopback0 (IP: 10.250.1.4) - Destination: s1-spine1 Loopback0 (IP: 10.250.1.1) | PASS | - |
| 174 | s1-leaf2 | Connectivity | VerifyReachability | Test network reachability to one or many destination IP(s). | Source: Loopback0 (IP: 10.250.1.4) - Destination: s1-spine2 Loopback0 (IP: 10.250.1.2) | PASS | - |
| 175 | s1-leaf2 | Connectivity | VerifyReachability | Test network reachability to one or many destination IP(s). | Source: P2P Interface Ethernet2 (IP: 172.16.1.5) - Destination: s1-spine1 Ethernet3 (IP: 172.16.1.4) | PASS | - |
| 176 | s1-leaf2 | Connectivity | VerifyReachability | Test network reachability to one or many destination IP(s). | Source: P2P Interface Ethernet3 (IP: 172.16.1.7) - Destination: s1-spine2 Ethernet3 (IP: 172.16.1.6) | PASS | - |
| 177 | s1-leaf2 | Hardware | VerifyEnvironmentCooling | Verifies the status of power supply fans and all fan trays. | Accepted States: 'ok' | SKIPPED | VerifyEnvironmentCooling test is not supported on cEOSLab. |
| 178 | s1-leaf2 | Hardware | VerifyEnvironmentPower | Verifies the power supplies status. | Accepted States: 'ok' | SKIPPED | VerifyEnvironmentPower test is not supported on cEOSLab. |
| 179 | s1-leaf2 | Hardware | VerifyTemperature | Verifies if the device temperature is within acceptable limits. | - | SKIPPED | VerifyTemperature test is not supported on cEOSLab. |
| 180 | s1-leaf2 | Hardware | VerifyTransceiversManufacturers | Verifies if all the transceivers come from approved manufacturers. | Accepted Manufacturers: 'Arista Networks', 'Arastra, Inc.', 'Not Present' | SKIPPED | VerifyTransceiversManufacturers test is not supported on cEOSLab. |
| 181 | s1-leaf2 | Interfaces | VerifyInterfacesStatus | Verifies the operational states of specified interfaces to ensure they match expected configurations. | Interface Ethernet1 - MLAG_s1-leaf1_Ethernet1 = 'up' | PASS | - |
| 182 | s1-leaf2 | Interfaces | VerifyInterfacesStatus | Verifies the operational states of specified interfaces to ensure they match expected configurations. | Interface Ethernet2 - P2P_s1-spine1_Ethernet3 = 'up' | PASS | - |
| 183 | s1-leaf2 | Interfaces | VerifyInterfacesStatus | Verifies the operational states of specified interfaces to ensure they match expected configurations. | Interface Ethernet3 - P2P_s1-spine2_Ethernet3 = 'up' | PASS | - |
| 184 | s1-leaf2 | Interfaces | VerifyInterfacesStatus | Verifies the operational states of specified interfaces to ensure they match expected configurations. | Interface Ethernet4 - SERVER_s1-host1_eth2 = 'up' | PASS | - |
| 185 | s1-leaf2 | Interfaces | VerifyInterfacesStatus | Verifies the operational states of specified interfaces to ensure they match expected configurations. | Interface Ethernet6 - MLAG_s1-leaf1_Ethernet6 = 'up' | PASS | - |
| 186 | s1-leaf2 | Interfaces | VerifyInterfacesStatus | Verifies the operational states of specified interfaces to ensure they match expected configurations. | Interface Loopback0 - ROUTER_ID = 'up' | PASS | - |
| 187 | s1-leaf2 | Interfaces | VerifyInterfacesStatus | Verifies the operational states of specified interfaces to ensure they match expected configurations. | Interface Loopback1 - VXLAN_TUNNEL_SOURCE = 'up' | PASS | - |
| 188 | s1-leaf2 | Interfaces | VerifyInterfacesStatus | Verifies the operational states of specified interfaces to ensure they match expected configurations. | Interface Port-Channel1 - MLAG_s1-leaf1_Port-Channel1 = 'up' | PASS | - |
| 189 | s1-leaf2 | Interfaces | VerifyInterfacesStatus | Verifies the operational states of specified interfaces to ensure they match expected configurations. | Interface Port-Channel4 - SERVER_s1-host1 = 'up' | PASS | - |
| 190 | s1-leaf2 | Interfaces | VerifyInterfacesStatus | Verifies the operational states of specified interfaces to ensure they match expected configurations. | Interface Vlan10 - Ten = 'up' | PASS | - |
| 191 | s1-leaf2 | Interfaces | VerifyInterfacesStatus | Verifies the operational states of specified interfaces to ensure they match expected configurations. | Interface Vlan20 - Twenty = 'up' | PASS | - |
| 192 | s1-leaf2 | Interfaces | VerifyInterfacesStatus | Verifies the operational states of specified interfaces to ensure they match expected configurations. | Interface Vlan3009 - MLAG_L3_VRF_OVERLAY = 'up' | PASS | - |
| 193 | s1-leaf2 | Interfaces | VerifyInterfacesStatus | Verifies the operational states of specified interfaces to ensure they match expected configurations. | Interface Vlan4093 - MLAG_L3 = 'up' | PASS | - |
| 194 | s1-leaf2 | Interfaces | VerifyInterfacesStatus | Verifies the operational states of specified interfaces to ensure they match expected configurations. | Interface Vlan4094 - MLAG = 'up' | PASS | - |
| 195 | s1-leaf2 | Interfaces | VerifyInterfacesStatus | Verifies the operational states of specified interfaces to ensure they match expected configurations. | Interface Vxlan1 = 'up' | PASS | - |
| 196 | s1-leaf2 | MLAG | VerifyMlagStatus | Verifies the health status of the MLAG configuration. | - | PASS | - |
| 197 | s1-leaf2 | Routing | VerifyRoutingProtocolModel | Verifies the configured routing protocol model. | Routing protocol model: multi-agent | PASS | - |
| 198 | s1-leaf2 | Routing | VerifyRoutingTableEntry | Verifies that the provided routes are present in the routing table of a specified VRF. | Route: 10.250.1.1 - Peer: s1-spine1 | PASS | - |
| 199 | s1-leaf2 | Routing | VerifyRoutingTableEntry | Verifies that the provided routes are present in the routing table of a specified VRF. | Route: 10.250.1.2 - Peer: s1-spine2 | PASS | - |
| 200 | s1-leaf2 | Routing | VerifyRoutingTableEntry | Verifies that the provided routes are present in the routing table of a specified VRF. | Route: 10.250.1.3 - Peer: s1-leaf1 | PASS | - |
| 201 | s1-leaf2 | Routing | VerifyRoutingTableEntry | Verifies that the provided routes are present in the routing table of a specified VRF. | Route: 10.250.1.4 - Peer: s1-leaf2 | PASS | - |
| 202 | s1-leaf2 | Routing | VerifyRoutingTableEntry | Verifies that the provided routes are present in the routing table of a specified VRF. | Route: 10.250.1.5 - Peer: s1-leaf3 | PASS | - |
| 203 | s1-leaf2 | Routing | VerifyRoutingTableEntry | Verifies that the provided routes are present in the routing table of a specified VRF. | Route: 10.250.1.6 - Peer: s1-leaf4 | PASS | - |
| 204 | s1-leaf2 | Routing | VerifyRoutingTableEntry | Verifies that the provided routes are present in the routing table of a specified VRF. | Route: 10.250.1.7 - Peer: s1-brdr1 | PASS | - |
| 205 | s1-leaf2 | Routing | VerifyRoutingTableEntry | Verifies that the provided routes are present in the routing table of a specified VRF. | Route: 10.250.1.8 - Peer: s1-brdr2 | PASS | - |
| 206 | s1-leaf2 | Routing | VerifyRoutingTableEntry | Verifies that the provided routes are present in the routing table of a specified VRF. | Route: 10.255.1.3 - Peer: s1-leaf1 | PASS | - |
| 207 | s1-leaf2 | Routing | VerifyRoutingTableEntry | Verifies that the provided routes are present in the routing table of a specified VRF. | Route: 10.255.1.5 - Peer: s1-leaf3 | PASS | - |
| 208 | s1-leaf2 | Routing | VerifyRoutingTableEntry | Verifies that the provided routes are present in the routing table of a specified VRF. | Route: 10.255.1.7 - Peer: s1-brdr1 | PASS | - |
| 209 | s1-leaf2 | System | VerifyNTP | Verifies if NTP is synchronised. | - | PASS | - |
| 210 | s1-leaf2 | System | VerifyReloadCause | Verifies the last reload cause of the device. | - | FAIL | Reload cause is: 'System reloaded due to Zero Touch Provisioning' |
| 211 | s1-leaf3 | BGP | VerifyBGPSpecificPeers | Verifies the health of specific BGP peer(s) for given address families. | BGP EVPN Peer: s1-spine1 (IP: 10.250.1.1) | PASS | - |
| 212 | s1-leaf3 | BGP | VerifyBGPSpecificPeers | Verifies the health of specific BGP peer(s) for given address families. | BGP EVPN Peer: s1-spine2 (IP: 10.250.1.2) | PASS | - |
| 213 | s1-leaf3 | BGP | VerifyBGPSpecificPeers | Verifies the health of specific BGP peer(s) for given address families. | BGP IPv4 Unicast Peer: s1-leaf4 (IP: 10.252.1.5) | PASS | - |
| 214 | s1-leaf3 | BGP | VerifyBGPSpecificPeers | Verifies the health of specific BGP peer(s) for given address families. | BGP IPv4 Unicast Peer: s1-spine1 (IP: 172.16.1.8) | PASS | - |
| 215 | s1-leaf3 | BGP | VerifyBGPSpecificPeers | Verifies the health of specific BGP peer(s) for given address families. | BGP IPv4 Unicast Peer: s1-spine2 (IP: 172.16.1.10) | PASS | - |
| 216 | s1-leaf3 | Connectivity | VerifyLLDPNeighbors | Verifies the connection status of the specified LLDP (Link Layer Discovery Protocol) neighbors. | Local: Ethernet1 - Remote: s1-leaf4 Ethernet1 | PASS | - |
| 217 | s1-leaf3 | Connectivity | VerifyLLDPNeighbors | Verifies the connection status of the specified LLDP (Link Layer Discovery Protocol) neighbors. | Local: Ethernet2 - Remote: s1-spine1 Ethernet4 | PASS | - |
| 218 | s1-leaf3 | Connectivity | VerifyLLDPNeighbors | Verifies the connection status of the specified LLDP (Link Layer Discovery Protocol) neighbors. | Local: Ethernet3 - Remote: s1-spine2 Ethernet4 | PASS | - |
| 219 | s1-leaf3 | Connectivity | VerifyLLDPNeighbors | Verifies the connection status of the specified LLDP (Link Layer Discovery Protocol) neighbors. | Local: Ethernet6 - Remote: s1-leaf4 Ethernet6 | PASS | - |
| 220 | s1-leaf3 | Connectivity | VerifyReachability | Test network reachability to one or many destination IP(s). | Source: Loopback0 (IP: 10.250.1.5) - Destination: s1-brdr1 Loopback0 (IP: 10.250.1.7) | PASS | - |
| 221 | s1-leaf3 | Connectivity | VerifyReachability | Test network reachability to one or many destination IP(s). | Source: Loopback0 (IP: 10.250.1.5) - Destination: s1-brdr2 Loopback0 (IP: 10.250.1.8) | PASS | - |
| 222 | s1-leaf3 | Connectivity | VerifyReachability | Test network reachability to one or many destination IP(s). | Source: Loopback0 (IP: 10.250.1.5) - Destination: s1-leaf1 Loopback0 (IP: 10.250.1.3) | PASS | - |
| 223 | s1-leaf3 | Connectivity | VerifyReachability | Test network reachability to one or many destination IP(s). | Source: Loopback0 (IP: 10.250.1.5) - Destination: s1-leaf2 Loopback0 (IP: 10.250.1.4) | PASS | - |
| 224 | s1-leaf3 | Connectivity | VerifyReachability | Test network reachability to one or many destination IP(s). | Source: Loopback0 (IP: 10.250.1.5) - Destination: s1-leaf3 Loopback0 (IP: 10.250.1.5) | PASS | - |
| 225 | s1-leaf3 | Connectivity | VerifyReachability | Test network reachability to one or many destination IP(s). | Source: Loopback0 (IP: 10.250.1.5) - Destination: s1-leaf4 Loopback0 (IP: 10.250.1.6) | PASS | - |
| 226 | s1-leaf3 | Connectivity | VerifyReachability | Test network reachability to one or many destination IP(s). | Source: Loopback0 (IP: 10.250.1.5) - Destination: s1-spine1 Loopback0 (IP: 10.250.1.1) | PASS | - |
| 227 | s1-leaf3 | Connectivity | VerifyReachability | Test network reachability to one or many destination IP(s). | Source: Loopback0 (IP: 10.250.1.5) - Destination: s1-spine2 Loopback0 (IP: 10.250.1.2) | PASS | - |
| 228 | s1-leaf3 | Connectivity | VerifyReachability | Test network reachability to one or many destination IP(s). | Source: P2P Interface Ethernet2 (IP: 172.16.1.9) - Destination: s1-spine1 Ethernet4 (IP: 172.16.1.8) | PASS | - |
| 229 | s1-leaf3 | Connectivity | VerifyReachability | Test network reachability to one or many destination IP(s). | Source: P2P Interface Ethernet3 (IP: 172.16.1.11) - Destination: s1-spine2 Ethernet4 (IP: 172.16.1.10) | PASS | - |
| 230 | s1-leaf3 | Hardware | VerifyEnvironmentCooling | Verifies the status of power supply fans and all fan trays. | Accepted States: 'ok' | SKIPPED | VerifyEnvironmentCooling test is not supported on cEOSLab. |
| 231 | s1-leaf3 | Hardware | VerifyEnvironmentPower | Verifies the power supplies status. | Accepted States: 'ok' | SKIPPED | VerifyEnvironmentPower test is not supported on cEOSLab. |
| 232 | s1-leaf3 | Hardware | VerifyTemperature | Verifies if the device temperature is within acceptable limits. | - | SKIPPED | VerifyTemperature test is not supported on cEOSLab. |
| 233 | s1-leaf3 | Hardware | VerifyTransceiversManufacturers | Verifies if all the transceivers come from approved manufacturers. | Accepted Manufacturers: 'Arista Networks', 'Arastra, Inc.', 'Not Present' | SKIPPED | VerifyTransceiversManufacturers test is not supported on cEOSLab. |
| 234 | s1-leaf3 | Interfaces | VerifyInterfacesStatus | Verifies the operational states of specified interfaces to ensure they match expected configurations. | Interface Ethernet1 - MLAG_s1-leaf4_Ethernet1 = 'up' | PASS | - |
| 235 | s1-leaf3 | Interfaces | VerifyInterfacesStatus | Verifies the operational states of specified interfaces to ensure they match expected configurations. | Interface Ethernet2 - P2P_s1-spine1_Ethernet4 = 'up' | PASS | - |
| 236 | s1-leaf3 | Interfaces | VerifyInterfacesStatus | Verifies the operational states of specified interfaces to ensure they match expected configurations. | Interface Ethernet3 - P2P_s1-spine2_Ethernet4 = 'up' | PASS | - |
| 237 | s1-leaf3 | Interfaces | VerifyInterfacesStatus | Verifies the operational states of specified interfaces to ensure they match expected configurations. | Interface Ethernet4 - SERVER_s1-host2_eth1 = 'up' | PASS | - |
| 238 | s1-leaf3 | Interfaces | VerifyInterfacesStatus | Verifies the operational states of specified interfaces to ensure they match expected configurations. | Interface Ethernet6 - MLAG_s1-leaf4_Ethernet6 = 'up' | PASS | - |
| 239 | s1-leaf3 | Interfaces | VerifyInterfacesStatus | Verifies the operational states of specified interfaces to ensure they match expected configurations. | Interface Loopback0 - ROUTER_ID = 'up' | PASS | - |
| 240 | s1-leaf3 | Interfaces | VerifyInterfacesStatus | Verifies the operational states of specified interfaces to ensure they match expected configurations. | Interface Loopback1 - VXLAN_TUNNEL_SOURCE = 'up' | PASS | - |
| 241 | s1-leaf3 | Interfaces | VerifyInterfacesStatus | Verifies the operational states of specified interfaces to ensure they match expected configurations. | Interface Port-Channel1 - MLAG_s1-leaf4_Port-Channel1 = 'up' | PASS | - |
| 242 | s1-leaf3 | Interfaces | VerifyInterfacesStatus | Verifies the operational states of specified interfaces to ensure they match expected configurations. | Interface Port-Channel4 - SERVER_s1-host2 = 'up' | PASS | - |
| 243 | s1-leaf3 | Interfaces | VerifyInterfacesStatus | Verifies the operational states of specified interfaces to ensure they match expected configurations. | Interface Vlan10 - Ten = 'up' | PASS | - |
| 244 | s1-leaf3 | Interfaces | VerifyInterfacesStatus | Verifies the operational states of specified interfaces to ensure they match expected configurations. | Interface Vlan20 - Twenty = 'up' | PASS | - |
| 245 | s1-leaf3 | Interfaces | VerifyInterfacesStatus | Verifies the operational states of specified interfaces to ensure they match expected configurations. | Interface Vlan3009 - MLAG_L3_VRF_OVERLAY = 'up' | PASS | - |
| 246 | s1-leaf3 | Interfaces | VerifyInterfacesStatus | Verifies the operational states of specified interfaces to ensure they match expected configurations. | Interface Vlan4093 - MLAG_L3 = 'up' | PASS | - |
| 247 | s1-leaf3 | Interfaces | VerifyInterfacesStatus | Verifies the operational states of specified interfaces to ensure they match expected configurations. | Interface Vlan4094 - MLAG = 'up' | PASS | - |
| 248 | s1-leaf3 | Interfaces | VerifyInterfacesStatus | Verifies the operational states of specified interfaces to ensure they match expected configurations. | Interface Vxlan1 = 'up' | PASS | - |
| 249 | s1-leaf3 | MLAG | VerifyMlagStatus | Verifies the health status of the MLAG configuration. | - | PASS | - |
| 250 | s1-leaf3 | Routing | VerifyRoutingProtocolModel | Verifies the configured routing protocol model. | Routing protocol model: multi-agent | PASS | - |
| 251 | s1-leaf3 | Routing | VerifyRoutingTableEntry | Verifies that the provided routes are present in the routing table of a specified VRF. | Route: 10.250.1.1 - Peer: s1-spine1 | PASS | - |
| 252 | s1-leaf3 | Routing | VerifyRoutingTableEntry | Verifies that the provided routes are present in the routing table of a specified VRF. | Route: 10.250.1.2 - Peer: s1-spine2 | PASS | - |
| 253 | s1-leaf3 | Routing | VerifyRoutingTableEntry | Verifies that the provided routes are present in the routing table of a specified VRF. | Route: 10.250.1.3 - Peer: s1-leaf1 | PASS | - |
| 254 | s1-leaf3 | Routing | VerifyRoutingTableEntry | Verifies that the provided routes are present in the routing table of a specified VRF. | Route: 10.250.1.4 - Peer: s1-leaf2 | PASS | - |
| 255 | s1-leaf3 | Routing | VerifyRoutingTableEntry | Verifies that the provided routes are present in the routing table of a specified VRF. | Route: 10.250.1.5 - Peer: s1-leaf3 | PASS | - |
| 256 | s1-leaf3 | Routing | VerifyRoutingTableEntry | Verifies that the provided routes are present in the routing table of a specified VRF. | Route: 10.250.1.6 - Peer: s1-leaf4 | PASS | - |
| 257 | s1-leaf3 | Routing | VerifyRoutingTableEntry | Verifies that the provided routes are present in the routing table of a specified VRF. | Route: 10.250.1.7 - Peer: s1-brdr1 | PASS | - |
| 258 | s1-leaf3 | Routing | VerifyRoutingTableEntry | Verifies that the provided routes are present in the routing table of a specified VRF. | Route: 10.250.1.8 - Peer: s1-brdr2 | PASS | - |
| 259 | s1-leaf3 | Routing | VerifyRoutingTableEntry | Verifies that the provided routes are present in the routing table of a specified VRF. | Route: 10.255.1.3 - Peer: s1-leaf1 | PASS | - |
| 260 | s1-leaf3 | Routing | VerifyRoutingTableEntry | Verifies that the provided routes are present in the routing table of a specified VRF. | Route: 10.255.1.5 - Peer: s1-leaf3 | PASS | - |
| 261 | s1-leaf3 | Routing | VerifyRoutingTableEntry | Verifies that the provided routes are present in the routing table of a specified VRF. | Route: 10.255.1.7 - Peer: s1-brdr1 | PASS | - |
| 262 | s1-leaf3 | System | VerifyNTP | Verifies if NTP is synchronised. | - | PASS | - |
| 263 | s1-leaf3 | System | VerifyReloadCause | Verifies the last reload cause of the device. | - | FAIL | Reload cause is: 'System reloaded due to Zero Touch Provisioning' |
| 264 | s1-leaf4 | BGP | VerifyBGPSpecificPeers | Verifies the health of specific BGP peer(s) for given address families. | BGP EVPN Peer: s1-spine1 (IP: 10.250.1.1) | PASS | - |
| 265 | s1-leaf4 | BGP | VerifyBGPSpecificPeers | Verifies the health of specific BGP peer(s) for given address families. | BGP EVPN Peer: s1-spine2 (IP: 10.250.1.2) | PASS | - |
| 266 | s1-leaf4 | BGP | VerifyBGPSpecificPeers | Verifies the health of specific BGP peer(s) for given address families. | BGP IPv4 Unicast Peer: s1-leaf3 (IP: 10.252.1.4) | PASS | - |
| 267 | s1-leaf4 | BGP | VerifyBGPSpecificPeers | Verifies the health of specific BGP peer(s) for given address families. | BGP IPv4 Unicast Peer: s1-spine1 (IP: 172.16.1.12) | PASS | - |
| 268 | s1-leaf4 | BGP | VerifyBGPSpecificPeers | Verifies the health of specific BGP peer(s) for given address families. | BGP IPv4 Unicast Peer: s1-spine2 (IP: 172.16.1.14) | PASS | - |
| 269 | s1-leaf4 | Connectivity | VerifyLLDPNeighbors | Verifies the connection status of the specified LLDP (Link Layer Discovery Protocol) neighbors. | Local: Ethernet1 - Remote: s1-leaf3 Ethernet1 | PASS | - |
| 270 | s1-leaf4 | Connectivity | VerifyLLDPNeighbors | Verifies the connection status of the specified LLDP (Link Layer Discovery Protocol) neighbors. | Local: Ethernet2 - Remote: s1-spine1 Ethernet5 | PASS | - |
| 271 | s1-leaf4 | Connectivity | VerifyLLDPNeighbors | Verifies the connection status of the specified LLDP (Link Layer Discovery Protocol) neighbors. | Local: Ethernet3 - Remote: s1-spine2 Ethernet5 | PASS | - |
| 272 | s1-leaf4 | Connectivity | VerifyLLDPNeighbors | Verifies the connection status of the specified LLDP (Link Layer Discovery Protocol) neighbors. | Local: Ethernet6 - Remote: s1-leaf3 Ethernet6 | PASS | - |
| 273 | s1-leaf4 | Connectivity | VerifyReachability | Test network reachability to one or many destination IP(s). | Source: Loopback0 (IP: 10.250.1.6) - Destination: s1-brdr1 Loopback0 (IP: 10.250.1.7) | PASS | - |
| 274 | s1-leaf4 | Connectivity | VerifyReachability | Test network reachability to one or many destination IP(s). | Source: Loopback0 (IP: 10.250.1.6) - Destination: s1-brdr2 Loopback0 (IP: 10.250.1.8) | PASS | - |
| 275 | s1-leaf4 | Connectivity | VerifyReachability | Test network reachability to one or many destination IP(s). | Source: Loopback0 (IP: 10.250.1.6) - Destination: s1-leaf1 Loopback0 (IP: 10.250.1.3) | PASS | - |
| 276 | s1-leaf4 | Connectivity | VerifyReachability | Test network reachability to one or many destination IP(s). | Source: Loopback0 (IP: 10.250.1.6) - Destination: s1-leaf2 Loopback0 (IP: 10.250.1.4) | PASS | - |
| 277 | s1-leaf4 | Connectivity | VerifyReachability | Test network reachability to one or many destination IP(s). | Source: Loopback0 (IP: 10.250.1.6) - Destination: s1-leaf3 Loopback0 (IP: 10.250.1.5) | PASS | - |
| 278 | s1-leaf4 | Connectivity | VerifyReachability | Test network reachability to one or many destination IP(s). | Source: Loopback0 (IP: 10.250.1.6) - Destination: s1-leaf4 Loopback0 (IP: 10.250.1.6) | PASS | - |
| 279 | s1-leaf4 | Connectivity | VerifyReachability | Test network reachability to one or many destination IP(s). | Source: Loopback0 (IP: 10.250.1.6) - Destination: s1-spine1 Loopback0 (IP: 10.250.1.1) | PASS | - |
| 280 | s1-leaf4 | Connectivity | VerifyReachability | Test network reachability to one or many destination IP(s). | Source: Loopback0 (IP: 10.250.1.6) - Destination: s1-spine2 Loopback0 (IP: 10.250.1.2) | PASS | - |
| 281 | s1-leaf4 | Connectivity | VerifyReachability | Test network reachability to one or many destination IP(s). | Source: P2P Interface Ethernet2 (IP: 172.16.1.13) - Destination: s1-spine1 Ethernet5 (IP: 172.16.1.12) | PASS | - |
| 282 | s1-leaf4 | Connectivity | VerifyReachability | Test network reachability to one or many destination IP(s). | Source: P2P Interface Ethernet3 (IP: 172.16.1.15) - Destination: s1-spine2 Ethernet5 (IP: 172.16.1.14) | PASS | - |
| 283 | s1-leaf4 | Hardware | VerifyEnvironmentCooling | Verifies the status of power supply fans and all fan trays. | Accepted States: 'ok' | SKIPPED | VerifyEnvironmentCooling test is not supported on cEOSLab. |
| 284 | s1-leaf4 | Hardware | VerifyEnvironmentPower | Verifies the power supplies status. | Accepted States: 'ok' | SKIPPED | VerifyEnvironmentPower test is not supported on cEOSLab. |
| 285 | s1-leaf4 | Hardware | VerifyTemperature | Verifies if the device temperature is within acceptable limits. | - | SKIPPED | VerifyTemperature test is not supported on cEOSLab. |
| 286 | s1-leaf4 | Hardware | VerifyTransceiversManufacturers | Verifies if all the transceivers come from approved manufacturers. | Accepted Manufacturers: 'Arista Networks', 'Arastra, Inc.', 'Not Present' | SKIPPED | VerifyTransceiversManufacturers test is not supported on cEOSLab. |
| 287 | s1-leaf4 | Interfaces | VerifyInterfacesStatus | Verifies the operational states of specified interfaces to ensure they match expected configurations. | Interface Ethernet1 - MLAG_s1-leaf3_Ethernet1 = 'up' | PASS | - |
| 288 | s1-leaf4 | Interfaces | VerifyInterfacesStatus | Verifies the operational states of specified interfaces to ensure they match expected configurations. | Interface Ethernet2 - P2P_s1-spine1_Ethernet5 = 'up' | PASS | - |
| 289 | s1-leaf4 | Interfaces | VerifyInterfacesStatus | Verifies the operational states of specified interfaces to ensure they match expected configurations. | Interface Ethernet3 - P2P_s1-spine2_Ethernet5 = 'up' | PASS | - |
| 290 | s1-leaf4 | Interfaces | VerifyInterfacesStatus | Verifies the operational states of specified interfaces to ensure they match expected configurations. | Interface Ethernet4 - SERVER_s1-host2_eth2 = 'up' | PASS | - |
| 291 | s1-leaf4 | Interfaces | VerifyInterfacesStatus | Verifies the operational states of specified interfaces to ensure they match expected configurations. | Interface Ethernet6 - MLAG_s1-leaf3_Ethernet6 = 'up' | PASS | - |
| 292 | s1-leaf4 | Interfaces | VerifyInterfacesStatus | Verifies the operational states of specified interfaces to ensure they match expected configurations. | Interface Loopback0 - ROUTER_ID = 'up' | PASS | - |
| 293 | s1-leaf4 | Interfaces | VerifyInterfacesStatus | Verifies the operational states of specified interfaces to ensure they match expected configurations. | Interface Loopback1 - VXLAN_TUNNEL_SOURCE = 'up' | PASS | - |
| 294 | s1-leaf4 | Interfaces | VerifyInterfacesStatus | Verifies the operational states of specified interfaces to ensure they match expected configurations. | Interface Port-Channel1 - MLAG_s1-leaf3_Port-Channel1 = 'up' | PASS | - |
| 295 | s1-leaf4 | Interfaces | VerifyInterfacesStatus | Verifies the operational states of specified interfaces to ensure they match expected configurations. | Interface Port-Channel4 - SERVER_s1-host2 = 'up' | PASS | - |
| 296 | s1-leaf4 | Interfaces | VerifyInterfacesStatus | Verifies the operational states of specified interfaces to ensure they match expected configurations. | Interface Vlan10 - Ten = 'up' | PASS | - |
| 297 | s1-leaf4 | Interfaces | VerifyInterfacesStatus | Verifies the operational states of specified interfaces to ensure they match expected configurations. | Interface Vlan20 - Twenty = 'up' | PASS | - |
| 298 | s1-leaf4 | Interfaces | VerifyInterfacesStatus | Verifies the operational states of specified interfaces to ensure they match expected configurations. | Interface Vlan3009 - MLAG_L3_VRF_OVERLAY = 'up' | PASS | - |
| 299 | s1-leaf4 | Interfaces | VerifyInterfacesStatus | Verifies the operational states of specified interfaces to ensure they match expected configurations. | Interface Vlan4093 - MLAG_L3 = 'up' | PASS | - |
| 300 | s1-leaf4 | Interfaces | VerifyInterfacesStatus | Verifies the operational states of specified interfaces to ensure they match expected configurations. | Interface Vlan4094 - MLAG = 'up' | PASS | - |
| 301 | s1-leaf4 | Interfaces | VerifyInterfacesStatus | Verifies the operational states of specified interfaces to ensure they match expected configurations. | Interface Vxlan1 = 'up' | PASS | - |
| 302 | s1-leaf4 | MLAG | VerifyMlagStatus | Verifies the health status of the MLAG configuration. | - | PASS | - |
| 303 | s1-leaf4 | Routing | VerifyRoutingProtocolModel | Verifies the configured routing protocol model. | Routing protocol model: multi-agent | PASS | - |
| 304 | s1-leaf4 | Routing | VerifyRoutingTableEntry | Verifies that the provided routes are present in the routing table of a specified VRF. | Route: 10.250.1.1 - Peer: s1-spine1 | PASS | - |
| 305 | s1-leaf4 | Routing | VerifyRoutingTableEntry | Verifies that the provided routes are present in the routing table of a specified VRF. | Route: 10.250.1.2 - Peer: s1-spine2 | PASS | - |
| 306 | s1-leaf4 | Routing | VerifyRoutingTableEntry | Verifies that the provided routes are present in the routing table of a specified VRF. | Route: 10.250.1.3 - Peer: s1-leaf1 | PASS | - |
| 307 | s1-leaf4 | Routing | VerifyRoutingTableEntry | Verifies that the provided routes are present in the routing table of a specified VRF. | Route: 10.250.1.4 - Peer: s1-leaf2 | PASS | - |
| 308 | s1-leaf4 | Routing | VerifyRoutingTableEntry | Verifies that the provided routes are present in the routing table of a specified VRF. | Route: 10.250.1.5 - Peer: s1-leaf3 | PASS | - |
| 309 | s1-leaf4 | Routing | VerifyRoutingTableEntry | Verifies that the provided routes are present in the routing table of a specified VRF. | Route: 10.250.1.6 - Peer: s1-leaf4 | PASS | - |
| 310 | s1-leaf4 | Routing | VerifyRoutingTableEntry | Verifies that the provided routes are present in the routing table of a specified VRF. | Route: 10.250.1.7 - Peer: s1-brdr1 | PASS | - |
| 311 | s1-leaf4 | Routing | VerifyRoutingTableEntry | Verifies that the provided routes are present in the routing table of a specified VRF. | Route: 10.250.1.8 - Peer: s1-brdr2 | PASS | - |
| 312 | s1-leaf4 | Routing | VerifyRoutingTableEntry | Verifies that the provided routes are present in the routing table of a specified VRF. | Route: 10.255.1.3 - Peer: s1-leaf1 | PASS | - |
| 313 | s1-leaf4 | Routing | VerifyRoutingTableEntry | Verifies that the provided routes are present in the routing table of a specified VRF. | Route: 10.255.1.5 - Peer: s1-leaf3 | PASS | - |
| 314 | s1-leaf4 | Routing | VerifyRoutingTableEntry | Verifies that the provided routes are present in the routing table of a specified VRF. | Route: 10.255.1.7 - Peer: s1-brdr1 | PASS | - |
| 315 | s1-leaf4 | System | VerifyNTP | Verifies if NTP is synchronised. | - | PASS | - |
| 316 | s1-leaf4 | System | VerifyReloadCause | Verifies the last reload cause of the device. | - | FAIL | Reload cause is: 'System reloaded due to Zero Touch Provisioning' |
| 317 | s1-spine1 | BGP | VerifyBGPSpecificPeers | Verifies the health of specific BGP peer(s) for given address families. | BGP EVPN Peer: s1-brdr1 (IP: 10.250.1.7) | PASS | - |
| 318 | s1-spine1 | BGP | VerifyBGPSpecificPeers | Verifies the health of specific BGP peer(s) for given address families. | BGP EVPN Peer: s1-brdr2 (IP: 10.250.1.8) | PASS | - |
| 319 | s1-spine1 | BGP | VerifyBGPSpecificPeers | Verifies the health of specific BGP peer(s) for given address families. | BGP EVPN Peer: s1-leaf1 (IP: 10.250.1.3) | PASS | - |
| 320 | s1-spine1 | BGP | VerifyBGPSpecificPeers | Verifies the health of specific BGP peer(s) for given address families. | BGP EVPN Peer: s1-leaf2 (IP: 10.250.1.4) | PASS | - |
| 321 | s1-spine1 | BGP | VerifyBGPSpecificPeers | Verifies the health of specific BGP peer(s) for given address families. | BGP EVPN Peer: s1-leaf3 (IP: 10.250.1.5) | PASS | - |
| 322 | s1-spine1 | BGP | VerifyBGPSpecificPeers | Verifies the health of specific BGP peer(s) for given address families. | BGP EVPN Peer: s1-leaf4 (IP: 10.250.1.6) | PASS | - |
| 323 | s1-spine1 | BGP | VerifyBGPSpecificPeers | Verifies the health of specific BGP peer(s) for given address families. | BGP IPv4 Unicast Peer: s1-brdr1 (IP: 172.16.1.17) | FAIL | AFI: ipv4 SAFI: unicast VRF: default Peer: 172.16.1.17 - Session state is not established - State: Active |
| 324 | s1-spine1 | BGP | VerifyBGPSpecificPeers | Verifies the health of specific BGP peer(s) for given address families. | BGP IPv4 Unicast Peer: s1-brdr2 (IP: 172.16.1.21) | PASS | - |
| 325 | s1-spine1 | BGP | VerifyBGPSpecificPeers | Verifies the health of specific BGP peer(s) for given address families. | BGP IPv4 Unicast Peer: s1-leaf1 (IP: 172.16.1.1) | PASS | - |
| 326 | s1-spine1 | BGP | VerifyBGPSpecificPeers | Verifies the health of specific BGP peer(s) for given address families. | BGP IPv4 Unicast Peer: s1-leaf2 (IP: 172.16.1.5) | PASS | - |
| 327 | s1-spine1 | BGP | VerifyBGPSpecificPeers | Verifies the health of specific BGP peer(s) for given address families. | BGP IPv4 Unicast Peer: s1-leaf3 (IP: 172.16.1.9) | PASS | - |
| 328 | s1-spine1 | BGP | VerifyBGPSpecificPeers | Verifies the health of specific BGP peer(s) for given address families. | BGP IPv4 Unicast Peer: s1-leaf4 (IP: 172.16.1.13) | PASS | - |
| 329 | s1-spine1 | Connectivity | VerifyLLDPNeighbors | Verifies the connection status of the specified LLDP (Link Layer Discovery Protocol) neighbors. | Local: Ethernet2 - Remote: s1-leaf1 Ethernet2 | PASS | - |
| 330 | s1-spine1 | Connectivity | VerifyLLDPNeighbors | Verifies the connection status of the specified LLDP (Link Layer Discovery Protocol) neighbors. | Local: Ethernet3 - Remote: s1-leaf2 Ethernet2 | PASS | - |
| 331 | s1-spine1 | Connectivity | VerifyLLDPNeighbors | Verifies the connection status of the specified LLDP (Link Layer Discovery Protocol) neighbors. | Local: Ethernet4 - Remote: s1-leaf3 Ethernet2 | PASS | - |
| 332 | s1-spine1 | Connectivity | VerifyLLDPNeighbors | Verifies the connection status of the specified LLDP (Link Layer Discovery Protocol) neighbors. | Local: Ethernet5 - Remote: s1-leaf4 Ethernet2 | PASS | - |
| 333 | s1-spine1 | Connectivity | VerifyLLDPNeighbors | Verifies the connection status of the specified LLDP (Link Layer Discovery Protocol) neighbors. | Local: Ethernet6 - Remote: s1-brdr1 Ethernet2 | FAIL | Port Ethernet6 (Neighbor: s1-brdr1.atd.lab, Neighbor Port: Ethernet2) - Wrong LLDP neighbors: s1-spine2.atd.lab/Ethernet6 |
| 334 | s1-spine1 | Connectivity | VerifyLLDPNeighbors | Verifies the connection status of the specified LLDP (Link Layer Discovery Protocol) neighbors. | Local: Ethernet8 - Remote: s1-brdr2 Ethernet2 | PASS | - |
| 335 | s1-spine1 | Connectivity | VerifyReachability | Test network reachability to one or many destination IP(s). | Source: P2P Interface Ethernet2 (IP: 172.16.1.0) - Destination: s1-leaf1 Ethernet2 (IP: 172.16.1.1) | PASS | - |
| 336 | s1-spine1 | Connectivity | VerifyReachability | Test network reachability to one or many destination IP(s). | Source: P2P Interface Ethernet3 (IP: 172.16.1.4) - Destination: s1-leaf2 Ethernet2 (IP: 172.16.1.5) | PASS | - |
| 337 | s1-spine1 | Connectivity | VerifyReachability | Test network reachability to one or many destination IP(s). | Source: P2P Interface Ethernet4 (IP: 172.16.1.8) - Destination: s1-leaf3 Ethernet2 (IP: 172.16.1.9) | PASS | - |
| 338 | s1-spine1 | Connectivity | VerifyReachability | Test network reachability to one or many destination IP(s). | Source: P2P Interface Ethernet5 (IP: 172.16.1.12) - Destination: s1-leaf4 Ethernet2 (IP: 172.16.1.13) | PASS | - |
| 339 | s1-spine1 | Connectivity | VerifyReachability | Test network reachability to one or many destination IP(s). | Source: P2P Interface Ethernet6 (IP: 172.16.1.16) - Destination: s1-brdr1 Ethernet2 (IP: 172.16.1.17) | FAIL | Host 172.16.1.17 (src: 172.16.1.16, vrf: default, size: 100B, repeat: 1) - Unreachable |
| 340 | s1-spine1 | Connectivity | VerifyReachability | Test network reachability to one or many destination IP(s). | Source: P2P Interface Ethernet8 (IP: 172.16.1.20) - Destination: s1-brdr2 Ethernet2 (IP: 172.16.1.21) | PASS | - |
| 341 | s1-spine1 | Hardware | VerifyEnvironmentCooling | Verifies the status of power supply fans and all fan trays. | Accepted States: 'ok' | SKIPPED | VerifyEnvironmentCooling test is not supported on cEOSLab. |
| 342 | s1-spine1 | Hardware | VerifyEnvironmentPower | Verifies the power supplies status. | Accepted States: 'ok' | SKIPPED | VerifyEnvironmentPower test is not supported on cEOSLab. |
| 343 | s1-spine1 | Hardware | VerifyTemperature | Verifies if the device temperature is within acceptable limits. | - | SKIPPED | VerifyTemperature test is not supported on cEOSLab. |
| 344 | s1-spine1 | Hardware | VerifyTransceiversManufacturers | Verifies if all the transceivers come from approved manufacturers. | Accepted Manufacturers: 'Arista Networks', 'Arastra, Inc.', 'Not Present' | SKIPPED | VerifyTransceiversManufacturers test is not supported on cEOSLab. |
| 345 | s1-spine1 | Interfaces | VerifyInterfacesStatus | Verifies the operational states of specified interfaces to ensure they match expected configurations. | Interface Ethernet2 - P2P_s1-leaf1_Ethernet2 = 'up' | PASS | - |
| 346 | s1-spine1 | Interfaces | VerifyInterfacesStatus | Verifies the operational states of specified interfaces to ensure they match expected configurations. | Interface Ethernet3 - P2P_s1-leaf2_Ethernet2 = 'up' | PASS | - |
| 347 | s1-spine1 | Interfaces | VerifyInterfacesStatus | Verifies the operational states of specified interfaces to ensure they match expected configurations. | Interface Ethernet4 - P2P_s1-leaf3_Ethernet2 = 'up' | PASS | - |
| 348 | s1-spine1 | Interfaces | VerifyInterfacesStatus | Verifies the operational states of specified interfaces to ensure they match expected configurations. | Interface Ethernet5 - P2P_s1-leaf4_Ethernet2 = 'up' | PASS | - |
| 349 | s1-spine1 | Interfaces | VerifyInterfacesStatus | Verifies the operational states of specified interfaces to ensure they match expected configurations. | Interface Ethernet6 - P2P_s1-brdr1_Ethernet2 = 'up' | PASS | - |
| 350 | s1-spine1 | Interfaces | VerifyInterfacesStatus | Verifies the operational states of specified interfaces to ensure they match expected configurations. | Interface Ethernet8 - P2P_s1-brdr2_Ethernet2 = 'up' | PASS | - |
| 351 | s1-spine1 | Interfaces | VerifyInterfacesStatus | Verifies the operational states of specified interfaces to ensure they match expected configurations. | Interface Loopback0 - ROUTER_ID = 'up' | PASS | - |
| 352 | s1-spine1 | Routing | VerifyRoutingProtocolModel | Verifies the configured routing protocol model. | Routing protocol model: multi-agent | PASS | - |
| 353 | s1-spine1 | System | VerifyNTP | Verifies if NTP is synchronised. | - | PASS | - |
| 354 | s1-spine1 | System | VerifyReloadCause | Verifies the last reload cause of the device. | - | FAIL | Reload cause is: 'System reloaded due to Zero Touch Provisioning' |
| 355 | s1-spine2 | BGP | VerifyBGPSpecificPeers | Verifies the health of specific BGP peer(s) for given address families. | BGP EVPN Peer: s1-brdr1 (IP: 10.250.1.7) | PASS | - |
| 356 | s1-spine2 | BGP | VerifyBGPSpecificPeers | Verifies the health of specific BGP peer(s) for given address families. | BGP EVPN Peer: s1-brdr2 (IP: 10.250.1.8) | PASS | - |
| 357 | s1-spine2 | BGP | VerifyBGPSpecificPeers | Verifies the health of specific BGP peer(s) for given address families. | BGP EVPN Peer: s1-leaf1 (IP: 10.250.1.3) | PASS | - |
| 358 | s1-spine2 | BGP | VerifyBGPSpecificPeers | Verifies the health of specific BGP peer(s) for given address families. | BGP EVPN Peer: s1-leaf2 (IP: 10.250.1.4) | PASS | - |
| 359 | s1-spine2 | BGP | VerifyBGPSpecificPeers | Verifies the health of specific BGP peer(s) for given address families. | BGP EVPN Peer: s1-leaf3 (IP: 10.250.1.5) | PASS | - |
| 360 | s1-spine2 | BGP | VerifyBGPSpecificPeers | Verifies the health of specific BGP peer(s) for given address families. | BGP EVPN Peer: s1-leaf4 (IP: 10.250.1.6) | PASS | - |
| 361 | s1-spine2 | BGP | VerifyBGPSpecificPeers | Verifies the health of specific BGP peer(s) for given address families. | BGP IPv4 Unicast Peer: s1-brdr1 (IP: 172.16.1.19) | FAIL | AFI: ipv4 SAFI: unicast VRF: default Peer: 172.16.1.19 - Session state is not established - State: Active |
| 362 | s1-spine2 | BGP | VerifyBGPSpecificPeers | Verifies the health of specific BGP peer(s) for given address families. | BGP IPv4 Unicast Peer: s1-brdr2 (IP: 172.16.1.23) | PASS | - |
| 363 | s1-spine2 | BGP | VerifyBGPSpecificPeers | Verifies the health of specific BGP peer(s) for given address families. | BGP IPv4 Unicast Peer: s1-leaf1 (IP: 172.16.1.3) | PASS | - |
| 364 | s1-spine2 | BGP | VerifyBGPSpecificPeers | Verifies the health of specific BGP peer(s) for given address families. | BGP IPv4 Unicast Peer: s1-leaf2 (IP: 172.16.1.7) | PASS | - |
| 365 | s1-spine2 | BGP | VerifyBGPSpecificPeers | Verifies the health of specific BGP peer(s) for given address families. | BGP IPv4 Unicast Peer: s1-leaf3 (IP: 172.16.1.11) | PASS | - |
| 366 | s1-spine2 | BGP | VerifyBGPSpecificPeers | Verifies the health of specific BGP peer(s) for given address families. | BGP IPv4 Unicast Peer: s1-leaf4 (IP: 172.16.1.15) | PASS | - |
| 367 | s1-spine2 | Connectivity | VerifyLLDPNeighbors | Verifies the connection status of the specified LLDP (Link Layer Discovery Protocol) neighbors. | Local: Ethernet2 - Remote: s1-leaf1 Ethernet3 | PASS | - |
| 368 | s1-spine2 | Connectivity | VerifyLLDPNeighbors | Verifies the connection status of the specified LLDP (Link Layer Discovery Protocol) neighbors. | Local: Ethernet3 - Remote: s1-leaf2 Ethernet3 | PASS | - |
| 369 | s1-spine2 | Connectivity | VerifyLLDPNeighbors | Verifies the connection status of the specified LLDP (Link Layer Discovery Protocol) neighbors. | Local: Ethernet4 - Remote: s1-leaf3 Ethernet3 | PASS | - |
| 370 | s1-spine2 | Connectivity | VerifyLLDPNeighbors | Verifies the connection status of the specified LLDP (Link Layer Discovery Protocol) neighbors. | Local: Ethernet5 - Remote: s1-leaf4 Ethernet3 | PASS | - |
| 371 | s1-spine2 | Connectivity | VerifyLLDPNeighbors | Verifies the connection status of the specified LLDP (Link Layer Discovery Protocol) neighbors. | Local: Ethernet6 - Remote: s1-brdr1 Ethernet3 | FAIL | Port Ethernet6 (Neighbor: s1-brdr1.atd.lab, Neighbor Port: Ethernet3) - Wrong LLDP neighbors: s1-spine1.atd.lab/Ethernet6 |
| 372 | s1-spine2 | Connectivity | VerifyLLDPNeighbors | Verifies the connection status of the specified LLDP (Link Layer Discovery Protocol) neighbors. | Local: Ethernet8 - Remote: s1-brdr2 Ethernet3 | PASS | - |
| 373 | s1-spine2 | Connectivity | VerifyReachability | Test network reachability to one or many destination IP(s). | Source: P2P Interface Ethernet2 (IP: 172.16.1.2) - Destination: s1-leaf1 Ethernet3 (IP: 172.16.1.3) | PASS | - |
| 374 | s1-spine2 | Connectivity | VerifyReachability | Test network reachability to one or many destination IP(s). | Source: P2P Interface Ethernet3 (IP: 172.16.1.6) - Destination: s1-leaf2 Ethernet3 (IP: 172.16.1.7) | PASS | - |
| 375 | s1-spine2 | Connectivity | VerifyReachability | Test network reachability to one or many destination IP(s). | Source: P2P Interface Ethernet4 (IP: 172.16.1.10) - Destination: s1-leaf3 Ethernet3 (IP: 172.16.1.11) | PASS | - |
| 376 | s1-spine2 | Connectivity | VerifyReachability | Test network reachability to one or many destination IP(s). | Source: P2P Interface Ethernet5 (IP: 172.16.1.14) - Destination: s1-leaf4 Ethernet3 (IP: 172.16.1.15) | PASS | - |
| 377 | s1-spine2 | Connectivity | VerifyReachability | Test network reachability to one or many destination IP(s). | Source: P2P Interface Ethernet6 (IP: 172.16.1.18) - Destination: s1-brdr1 Ethernet3 (IP: 172.16.1.19) | FAIL | Host 172.16.1.19 (src: 172.16.1.18, vrf: default, size: 100B, repeat: 1) - Unreachable |
| 378 | s1-spine2 | Connectivity | VerifyReachability | Test network reachability to one or many destination IP(s). | Source: P2P Interface Ethernet8 (IP: 172.16.1.22) - Destination: s1-brdr2 Ethernet3 (IP: 172.16.1.23) | PASS | - |
| 379 | s1-spine2 | Hardware | VerifyEnvironmentCooling | Verifies the status of power supply fans and all fan trays. | Accepted States: 'ok' | SKIPPED | VerifyEnvironmentCooling test is not supported on cEOSLab. |
| 380 | s1-spine2 | Hardware | VerifyEnvironmentPower | Verifies the power supplies status. | Accepted States: 'ok' | SKIPPED | VerifyEnvironmentPower test is not supported on cEOSLab. |
| 381 | s1-spine2 | Hardware | VerifyTemperature | Verifies if the device temperature is within acceptable limits. | - | SKIPPED | VerifyTemperature test is not supported on cEOSLab. |
| 382 | s1-spine2 | Hardware | VerifyTransceiversManufacturers | Verifies if all the transceivers come from approved manufacturers. | Accepted Manufacturers: 'Arista Networks', 'Arastra, Inc.', 'Not Present' | SKIPPED | VerifyTransceiversManufacturers test is not supported on cEOSLab. |
| 383 | s1-spine2 | Interfaces | VerifyInterfacesStatus | Verifies the operational states of specified interfaces to ensure they match expected configurations. | Interface Ethernet2 - P2P_s1-leaf1_Ethernet3 = 'up' | PASS | - |
| 384 | s1-spine2 | Interfaces | VerifyInterfacesStatus | Verifies the operational states of specified interfaces to ensure they match expected configurations. | Interface Ethernet3 - P2P_s1-leaf2_Ethernet3 = 'up' | PASS | - |
| 385 | s1-spine2 | Interfaces | VerifyInterfacesStatus | Verifies the operational states of specified interfaces to ensure they match expected configurations. | Interface Ethernet4 - P2P_s1-leaf3_Ethernet3 = 'up' | PASS | - |
| 386 | s1-spine2 | Interfaces | VerifyInterfacesStatus | Verifies the operational states of specified interfaces to ensure they match expected configurations. | Interface Ethernet5 - P2P_s1-leaf4_Ethernet3 = 'up' | PASS | - |
| 387 | s1-spine2 | Interfaces | VerifyInterfacesStatus | Verifies the operational states of specified interfaces to ensure they match expected configurations. | Interface Ethernet6 - P2P_s1-brdr1_Ethernet3 = 'up' | PASS | - |
| 388 | s1-spine2 | Interfaces | VerifyInterfacesStatus | Verifies the operational states of specified interfaces to ensure they match expected configurations. | Interface Ethernet8 - P2P_s1-brdr2_Ethernet3 = 'up' | PASS | - |
| 389 | s1-spine2 | Interfaces | VerifyInterfacesStatus | Verifies the operational states of specified interfaces to ensure they match expected configurations. | Interface Loopback0 - ROUTER_ID = 'up' | PASS | - |
| 390 | s1-spine2 | Routing | VerifyRoutingProtocolModel | Verifies the configured routing protocol model. | Routing protocol model: multi-agent | PASS | - |
| 391 | s1-spine2 | System | VerifyNTP | Verifies if NTP is synchronised. | - | PASS | - |
| 392 | s1-spine2 | System | VerifyReloadCause | Verifies the last reload cause of the device. | - | FAIL | Reload cause is: 'System reloaded due to Zero Touch Provisioning' |
