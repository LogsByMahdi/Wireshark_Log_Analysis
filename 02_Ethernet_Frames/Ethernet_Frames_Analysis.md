# Using Wireshark to Examine Ethernet Frames

## Objectives

# Part 1: Examine the Header Fields in an Ethernet II Frame
# Part 2: Use Wireshark to Capture and Analyze Ethernet Frames

# ---

# Background

When upper-layer protocols communicate, data flows down the OSI layers and is encapsulated into a Layer 2 frame.
For Ethernet LANs, encapsulation uses the \*\*Ethernet II\*\* frame format.

# In this lab, I analyzed Ethernet II frames using Wireshark to understand:

- Frame fields (destination, source, type, data, FCS)
- ARP request/reply traffic
- ICMP (ping) traffic between hosts
- Differences between local and remote traffic

# ---

# ## Required Resources

# - CyberOps Workstation VM
# - Mininet topology provided in the lab support files
# - Wireshark installed on the VM

# ---

# ## Part 1: Examine the Header Fields in an Ethernet II Frame

# ### Step 1: Review Ethernet II Header Fields


# ---


# ### Step 2: Analyze an ARP Request in Wireshark

# Opened a capture of ARP and ICMP traffic between a PC and its default gateway.

# 


