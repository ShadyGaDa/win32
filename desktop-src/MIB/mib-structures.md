---
title: MIB Structures
description: To get and set MIB variables.
ms.assetid: '811a1e41-efce-4e9c-8329-1c6929e12a8d'
---

# MIB Structures

Use the following structures with MIB-specific functions to get and set MIB variables. These structures are defined in Iprtrmib.h and Netioapi.h.



| Structure                                                              | Description                                                                                                                                                                                                                                 |
|------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**MIB\_ANYCASTIPADDRESS\_ROW**](mib-anycastipaddress-row.md)         | Stores information about an anycast IP address.                                                                                                                                                                                             |
| [**MIB\_ANYCASTIPADDRESS\_TABLE**](mib-anycastipaddress-table.md)     | Contains a table of anycast IP address entries.                                                                                                                                                                                             |
| [**MIB\_BEST\_IF**](mib-best-if.md)                                   | Stores the index of the interface that has the best route to a particular destination address.                                                                                                                                              |
| [**MIB\_BOUNDARYROW**](mib-boundaryrow.md)                            | Contains the IPv4 group address value and mask for a multicast boundary.                                                                                                                                                                    |
| [**MIB\_ICMP**](mib-icmp.md)                                          | Contains the Internet Control Message Protocol (ICMP) statistics for a particular computer.                                                                                                                                                 |
| [**MIB\_ICMP\_EX**](mib-icmp-ex.md)                                   | Contains the extended ICMP statistics for a particular computer.                                                                                                                                                                            |
| [**MIB\_IFNUMBER**](mib-ifnumber.md)                                  | Stores the number of interfaces on a particular computer.                                                                                                                                                                                   |
| [**MIB\_IFROW**](mib-ifrow.md)                                        | Stores information about a particular interface.                                                                                                                                                                                            |
| [**MIB\_IFSTACK\_ROW**](mib-ifstack-row.md)                           | Represents the relationship between two network interfaces.                                                                                                                                                                                 |
| [**MIB\_IFSTACK\_TABLE**](mib-ifstack-table.md)                       | Contains a table of network interface stack row entries. This specifies the relationship of the network interfaces on an interface stack.                                                                                                   |
| [**MIB\_IFSTATUS**](mib-ifstatus.md)                                  | Stores status information for a particular interface.                                                                                                                                                                                       |
| [**MIB\_IFTABLE**](mib-iftable.md)                                    | Contains a table of interface entries.                                                                                                                                                                                                      |
| [**MIB\_IF\_ROW2**](mib-if-row2.md)                                   | Stores information about a particular interface.                                                                                                                                                                                            |
| [**MIB\_IF\_TABLE2**](mib-if-table2.md)                               | Contains a table of interface entries.                                                                                                                                                                                                      |
| [**MIB\_INVERTEDIFSTACK\_ROW**](mib-invertedifstack-row.md)           | Represents the relationship between two network interfaces.                                                                                                                                                                                 |
| [**MIB\_INVERTEDIFSTACK\_TABLE**](mib-invertedifstack-table.md)       | Contains a table of inverted network interface stack row entries. This specifies the relationship of the network interfaces on an interface stack in reverse order.                                                                         |
| [**MIB\_IPADDRROW**](mib-ipaddrrow.md)                                | Specifies information for a particular IPv4 address in the [**MIB\_IPADDRTABLE**](mib-ipaddrtable.md) structure.                                                                                                                           |
| [**MIB\_IPADDRTABLE**](mib-ipaddrtable.md)                            | Contains a table of IPv4 address entries.                                                                                                                                                                                                   |
| [**MIB\_IPFORWARD\_ROW2**](mib-ipforward-row2.md)                     | Stores information about an IP route entry.                                                                                                                                                                                                 |
| [**MIB\_IPFORWARD\_TABLE2**](mib-ipforward-table2.md)                 | Contains a table of IP route entries.                                                                                                                                                                                                       |
| [**MIB\_IPFORWARDNUMBER**](mib-ipforwardnumber.md)                    | Stores the number of routes in a particular IP routing table.                                                                                                                                                                               |
| [**MIB\_IPFORWARDROW**](mib-ipforwardrow.md)                          | Contains information that describes an IPv4 network route.                                                                                                                                                                                  |
| [**MIB\_IPFORWARDTABLE**](mib-ipforwardtable.md)                      | Contains a table of IPv4 route entries.                                                                                                                                                                                                     |
| [**MIB\_IPINTERFACE\_ROW**](mib-ipinterface-row.md)                   | Stores interface management information for a particular IP address family on a network interface.                                                                                                                                          |
| [**MIB\_IPINTERFACE\_TABLE**](mib-ipinterface-table.md)               | contains a table of IP interface entries.                                                                                                                                                                                                   |
| [**MIB\_IPMCAST\_BOUNDARY**](mib-ipmcast-boundary.md)                 | Contains a row in a [**MIB\_IPMCAST\_BOUNDARY\_TABLE**](mib-ipmcast-boundary-table.md) structure that lists a router's scoped IPv4 multicast address boundaries.                                                                           |
| [**MIB\_IPMCAST\_BOUNDARY\_TABLE**](mib-ipmcast-boundary-table.md)    | Contains a list of a router's scoped IPv4 multicast address boundaries.                                                                                                                                                                     |
| [**MIB\_IPMCAST\_GLOBAL**](mib-ipmcast-global.md)                     | Stores global information for IP multicast on a particular computer.                                                                                                                                                                        |
| [**MIB\_IPMCAST\_IF\_ENTRY**](mib-ipmcast-if-entry.md)                | Stores information about an IP multicast interface.                                                                                                                                                                                         |
| [**MIB\_IPMCAST\_IF\_TABLE**](mib-ipmcast-if-table.md)                | Contains a table of IP multicast interface entries.                                                                                                                                                                                         |
| [**MIB\_IPMCAST\_MFE**](mib-ipmcast-mfe.md)                           | Stores the information for an IP Multicast Forwarding Entry (MFE).                                                                                                                                                                          |
| [**MIB\_IPMCAST\_MFE\_STATS**](mib-ipmcast-mfe-stats.md)              | Stores the statistics associated with an IP Multicast Forwarding Entry.                                                                                                                                                                     |
| [**MIB\_IPMCAST\_MFE\_STATS\_EX**](mib-ipmcast-mfe-stats-ex.md)       | Stores the extended statistics associated with an IP Multicast Forwarding Entry.                                                                                                                                                            |
| [**MIB\_IPMCAST\_OIF**](mib-ipmcast-oif.md)                           | Stores the information required to send an outgoing IP multicast packet.                                                                                                                                                                    |
| [**MIB\_IPMCAST\_OIF\_STATS**](mib-ipmcast-oif-stats.md)              | Stores the statistics that are associated with an outgoing multicast interface.                                                                                                                                                             |
| [**MIB\_IPMCAST\_SCOPE**](mib-ipmcast-scope.md)                       | Contains a multicast scope name and the associated IPv4 multicast group address and mask that define the scope.                                                                                                                             |
| [**MIB\_IPNET\_ROW2**](mib-ipnet-row2.md)                             | Stores information about a neighbor IP address.                                                                                                                                                                                             |
| [**MIB\_IPNET\_TABLE2**](mib-ipnet-table2.md)                         | Contains a table of neighbor IP address entries.                                                                                                                                                                                            |
| [**MIB\_IPNETROW**](mib-ipnetrow.md)                                  | Contains information for an Address Resolution Protocol (ARP) table entry.                                                                                                                                                                  |
| [**MIB\_IPNETTABLE**](mib-ipnettable.md)                              | Contains a table of ARP entries.                                                                                                                                                                                                            |
| [**MIB\_IPPATH\_ROW**](mib-ippath-row.md)                             | Stores information about an IP path entry.                                                                                                                                                                                                  |
| [**MIB\_IPPATH\_TABLE**](mib-ippath-table.md)                         | Contains a table of IP path entries.                                                                                                                                                                                                        |
| [**MIB\_IPSTATS**](mib-ipstats.md)                                    | Stores information about the IP protocol running on a particular computer.                                                                                                                                                                  |
| [**MIB\_MCAST\_LIMIT\_ROW**](mib-mcast-limit-row.md)                  | Contains the configurable limit information from a corresponding structure.                                                                                                                                                                 |
| [**MIB\_MFE\_STATS\_TABLE**](mib-mfe-stats-table.md)                  | Contains [**MIB\_IPMCAST\_IF\_ENTRY**](mib-ipmcast-if-entry.md)a table of Multicast Forwarding Entries (MFEs).                                                                                                                             |
| [**MIB\_MFE\_STATS\_TABLE\_EX**](mib-mfe-stats-table-ex.md)           | Contains a table of extended statistics for Multicast Forwarding Entries (MFEs).                                                                                                                                                            |
| [**MIB\_MFE\_TABLE**](mib-mfe-table.md)                               | Stores statistics for a group of Multicast Forwarding Entries (MFEs).                                                                                                                                                                       |
| [**MIB\_MULTICASTIPADDRESS\_ROW**](mib-multicastipaddress-row.md)     | Stores information about a multicast IP address.                                                                                                                                                                                            |
| [**MIB\_MULTICASTIPADDRESS\_TABLE**](mib-multicastipaddress-table.md) | Contains a table of multicast IP address entries.                                                                                                                                                                                           |
| [**MIB\_OPAQUE\_INFO**](mib-opaque-info.md)                           | Contains information returned from a MIB opaque query.                                                                                                                                                                                      |
| [**MIB\_OPAQUE\_QUERY**](mib-opaque-query.md)                         | Contains information for a MIB opaque query.                                                                                                                                                                                                |
| [**MIB\_PROXYARP**](mib-proxyarp.md)                                  | Stores information for a Proxy Address Resolution Protocol (PARP) entry.                                                                                                                                                                    |
| [**MIB\_TCP6ROW**](mib-tcp6row.md)                                    | Contains information that describes an IPv6 TCP connection.                                                                                                                                                                                 |
| [**MIB\_TCP6ROW2**](mib-tcp6row2.md)                                  | Contains information that describes an IPv6 TCP connection.                                                                                                                                                                                 |
| [**MIB\_TCP6ROW\_OWNER\_MODULE**](mib-tcp6row-owner-module.md)        | Contains information that describes an IPv6 TCP connection bound to a specific process ID (PID) with ownership data.                                                                                                                        |
| [**MIB\_TCP6ROW\_OWNER\_PID**](mib-tcp6row-owner-pid.md)              | Contains information that describes that describes an IPv6 TCP connection associated with a specific process ID (PID).                                                                                                                      |
| [**MIB\_TCP6TABLE**](mib-tcp6table.md)                                | Contains a table of IPv6 TCP connections on the local computer.                                                                                                                                                                             |
| [**MIB\_TCP6TABLE2**](mib-tcp6table2.md)                              | Contains a table of IPv6 TCP connections on the local computer.                                                                                                                                                                             |
| [**MIB\_TCP6TABLE\_OWNER\_MODULE**](mib-tcp6table-owner-module.md)    | Contains a table of IPv6 TCP connections on the local computer with the associated process ID and any available ownership data.                                                                                                             |
| [**MIB\_TCP6TABLE\_OWNER\_PID**](mib-tcp6table-owner-pid.md)          | Contains a table of IPv6 TCP connections on the local computer with the associated process ID bound to each TCP connection.                                                                                                                 |
| [**MIB\_TCPROW**](mib-tcprow.md)                                      | Contains information that describes an IPv4 TCP connection.                                                                                                                                                                                 |
| [**MIB\_TCPROW2**](mib-tcprow2.md)                                    | Contains information that describes an IPv4 TCP connection.                                                                                                                                                                                 |
| [**MIB\_TCPROW\_OWNER\_MODULE**](mib-tcprow-owner-module.md)          | Contains information that describes an IPv4 TCP connection with ownership data, IPv6 addresses, ports used by the TCP connection, and the specific process ID associated with connection.                                                   |
| [**MIB\_TCPROW\_OWNER\_PID**](mib-tcprow-owner-pid.md)                | Contains information that describes an IPv4 TCP connection with IPv6 addresses, ports used by the TCP connection, and the specific process ID associated with connection.                                                                   |
| [**MIB\_TCPTABLE**](mib-tcptable.md)                                  | Contains a table of IPv4 TCP connections.                                                                                                                                                                                                   |
| [**MIB\_TCPTABLE2**](mib-tcptable2.md)                                | Contains a table of IPv4 TCP connections.                                                                                                                                                                                                   |
| [**MIB\_TCPTABLE\_OWNER\_MODULE**](mib-tcptable-owner-module.md)      | Contains a table of IPv4 TCP connections on the local computer with the associated process ID, and any available ownership data.                                                                                                            |
| [**MIB\_TCPTABLE\_OWNER\_PID**](mib-tcptable-owner-pid.md)            | Contains a table of IPv4 TCP connections on the local computer with the associated process ID bound to each TCP connection.                                                                                                                 |
| [**MIB\_TCPSTATS**](mib-tcpstats.md)                                  | Contains statistics for the TCP protocol running on the local computer.                                                                                                                                                                     |
| [**MIB\_TCPSTATS2**](mib-tcpstats2.md)                                | Contains statistics for the TCP protocol running on the local computer, using 64-bit counters.                                                                                                                                              |
| [**MIB\_UDP6ROW**](mib-udp6row.md)                                    | Contains an entry from the User Datagram Protocol (UDP) listener table for IPv4 on the local computer.                                                                                                                                      |
| [**MIB\_UDP6ROW\_OWNER\_MODULE**](mib-udp6row-owner-module.md)        | Contains an entry from the UDP listener table for IPv4 on the local computer. The entry also includes any available ownership data and the process ID that issued the call to the [**bind**](https://msdn.microsoft.com/library/windows/desktop/ms737550) function for the UDP endpoint. |
| [**MIB\_UDP6ROW\_OWNER\_PID**](mib-udp6row-owner-pid.md)              | Contains an entry from the UDP listener table for IPv4 on the local computer. The entry also includes the process ID that issued the call to the [**bind**](https://msdn.microsoft.com/library/windows/desktop/ms737550) function for the UDP endpoint.                                  |
| [**MIB\_UDP6TABLE**](mib-udp6table.md)                                | Contains the UDP listener table for IPv6 on the local computer.                                                                                                                                                                             |
| [**MIB\_UDP6TABLE\_OWNER\_MODULE**](mib-udp6table-owner-module.md)    | Contains the UDP listener table for IPv6 on the local computer. The table also includes any available ownership data and the process ID that issued the call to the [**bind**](https://msdn.microsoft.com/library/windows/desktop/ms737550) function for each UDP endpoint.              |
| [**MIB\_UDP6TABLE\_OWNER\_PID**](mib-udp6table-owner-pid.md)          | Contains the UDP listener table for IPv6 on the local computer. The table also includes the process ID that issued the call to the [**bind**](https://msdn.microsoft.com/library/windows/desktop/ms737550) function for each UDP endpoint.                                               |
| [**MIB\_UDPROW**](mib-udprow.md)                                      | Contains an entry from the UDP listener table for IPv4 on the local computer.                                                                                                                                                               |
| [**MIB\_UDPROW\_OWNER\_MODULE**](mib-udprow-owner-module.md)          | Contains an entry from the UDP listener table for IPv4 on the local computer. The entry also includes any available ownership data and the process ID that issued the call to the [**bind**](https://msdn.microsoft.com/library/windows/desktop/ms737550) function for the UDP endpoint. |
| [**MIB\_UDPROW\_OWNER\_PID**](mib-udprow-owner-pid.md)                | Contains an entry from the UDP listener table for IPv4 on the local computer. The entry also includes the process ID that issued the call to the [**bind**](https://msdn.microsoft.com/library/windows/desktop/ms737550) function for the UDP endpoint.                                  |
| [**MIB\_UDPSTATS**](mib-udpstats.md)                                  | Contains statistics for the UDP running on the local computer.                                                                                                                                                                              |
| [**MIB\_UDPSTATS2**](mib-udpstats2.md)                                | Contains statistics for the UDP running on the local computer, using 64-bit counters.                                                                                                                                                       |
| [**MIB\_UDPTABLE**](mib-udptable.md)                                  | Contains the UDP listener table for IPv4 on the local computer.                                                                                                                                                                             |
| [**MIB\_UDPTABLE\_OWNER\_MODULE**](mib-udptable-owner-module.md)      | Contains the UDP listener table for IPv4 on the local computer. The table also includes any available ownership data and the process ID that issued the call to the [**bind**](https://msdn.microsoft.com/library/windows/desktop/ms737550) function for each UDP endpoint.              |
| [**MIB\_UDPTABLE\_OWNER\_PID**](mib-udptable-owner-pid.md)            | Contains the UDP listener table for IPv4 on the local computer. The table also includes the process ID that issued the call to the [**bind**](https://msdn.microsoft.com/library/windows/desktop/ms737550) function for each UDP endpoint.                                               |
| [**MIB\_UNICASTIPADDRESS\_ROW**](mib-unicastipaddress-row.md)         | Stores information about a unicast IP address.                                                                                                                                                                                              |
| [**MIB\_UNICASTIPADDRESS\_TABLE**](mib-unicastipaddress-table.md)     | Contains a table of unicast IP address entries.                                                                                                                                                                                             |
| [**MIBICMPINFO**](mibicmpinfo.md)                                     | Contains ICMP statistics for a particular computer.                                                                                                                                                                                         |
| [**MIBICMPSTATS**](mibicmpstats.md)                                   | Contains statistics for either incoming or outgoing ICMP messages on a particular computer.                                                                                                                                                 |
| [**MIBICMPSTATS\_EX**](mibicmpstats-ex.md)                            | Contains extended statistics for either incoming or outgoing ICMP messages on a particular computer.                                                                                                                                        |
| [**NL\_INTERFACE\_OFFLOAD\_ROD**](nl-interface-offload-rod.md)        | Specifies a set of flags that indicate the offload capabilities for an IP interface.                                                                                                                                                        |



 

 

 



