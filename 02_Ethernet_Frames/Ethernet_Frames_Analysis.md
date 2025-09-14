# \# Using Wireshark to Examine Ethernet Frames

# 

# \## Objectives

# \- \*\*Part 1:\*\* Examine the Header Fields in an Ethernet II Frame  

# \- \*\*Part 2:\*\* Use Wireshark to Capture and Analyze Ethernet Frames  

# 

# ---

# 

# \## Background / Scenario



# When upper-layer protocols communicate, data flows down the OSI layers and is encapsulated into a Layer 2 frame.  

# For Ethernet LANs, encapsulation uses the \*\*Ethernet II\*\* frame format.

# 

# In this lab, I analyzed Ethernet II frames using Wireshark to understand:  



# \- Frame fields (destination, source, type, data, FCS)  

# \- ARP request/reply traffic  

# \- ICMP (ping) traffic between hosts  

# \- Differences between local and remote traffic  

# 

# ---

# 

# \## Required Resources

# \- CyberOps Workstation VM  

# \- Mininet topology provided in the lab support files  

# \- Wireshark installed on the VM  

# 

# ---

# 

# \## Part 1: Examine the Header Fields in an Ethernet II Frame

# 

# \### Step 1: Review Ethernet II Header Fields

# | Field      | Length     | Description |

# |------------|------------|-------------|

# | Preamble   | 8 bytes    | Synchronization bits (not shown in Wireshark) |

# | Destination Address | 6 bytes | MAC address of the destination |

# | Source Address     | 6 bytes | MAC address of the sender |

# | Frame Type         | 2 bytes | Identifies the upper-layer protocol (e.g., 0x0800 = IPv4, 0x0806 = ARP) |

# | Data               | 46–1500 bytes | Encapsulated payload |

# | FCS                | 4 bytes | Frame Check Sequence (error detection, not shown in Wireshark) |

# 

# ---

# 

# \### Step 2: Analyze an ARP Request in Wireshark

# Opened a capture of ARP and ICMP traffic between a PC and its default gateway.

# 

# \*\*Screenshot to include:\*\* Wireshark view of ARP request frame.  

# 

# | Field              | Value |

# |--------------------|-------|

# | Destination MAC    | ff:ff:ff:ff:ff:ff (Broadcast) |

# | Source MAC         | f4:8c:50:62:62:6d |

# | Frame Type         | 0x0806 (ARP) |

# | Data               | ARP |

# | FCS                | Not displayed |

# 

# \*\*Questions and Answers:\*\*  

# \- What is significant about the destination address?  

# &nbsp; → It’s a broadcast, sent to all hosts on the LAN.  

# \- Why does the PC send out a broadcast ARP before pinging?  

# &nbsp; → To learn the MAC address of the default gateway.  

# \- What is the source MAC address?  

# &nbsp; → f4:8c:50:62:62:6d  

# \- What is the Vendor ID (OUI)?  

# &nbsp; → IntelCor (first 6 hex digits)  

# \- What is the NIC serial number?  

# &nbsp; → 62:62:6d  

# 

# ---

# 

# \## Part 2: Use Wireshark to Capture and Analyze Ethernet Frames

# 

# \### Step 1: Network Configuration of Host H3

# Ran the following in Mininet:

# 

# ```bash

# ip address

# netstat -r



