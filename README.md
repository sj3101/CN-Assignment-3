# CN Assignment-3

## Submitted By
- **Name:** Srshti Jain  
- **Roll Number:** 2301730107  
- **Program:** B.Tech CSE (AI/ML)  
- **Section:** B  
- **Course:** Computer Networks Lab  

---

# Routing Tables

## 1. Routing Information Protocol (RIP)

## Copper Straight-Through Connections

| From | To | Port/Interface |
|------|----|----------------|
| PC0 | S1 | Fa0/1 |
| PC1 | S1 | Fa0/2 |
| S1 | R0 | Fa0/24 → Fa2/0 |
| PC2 | S2 | Fa0/1 |
| PC3 | S2 | Fa0/2 |
| S2 | R1 | Fa0/24 → Fa2/0 |
| PC4 | S3 | Fa0/1 |
| PC5 | S3 | Fa0/2 |
| S3 | R2 | Fa0/24 → Fa2/0 |

## Serial DTE Connections

| From | To | Port/Interface |
|------|----|----------------|
| R0 | R1 | Se0/0 ↔ Se1/0 |
| R1 | R2 | Se0/0 ↔ Se1/0 |

---

# Network Design

The network topology was created using **Cisco Packet Tracer** and consists of:

- Three Routers: **R0, R1, R2**
- Three Switches: **S1, S2, S3**
- Multiple End Devices: **PCs**

Each router is connected to a switch, and each switch connects to multiple PCs, forming three separate Local Area Networks (LANs).

The routers are interconnected using serial DTE links to allow communication between different networks.

IP addresses were assigned to all devices, and routing protocols such as **RIP** and **OSPF** were configured for end-to-end communication.

## Advantages of the Design

- Proper network segmentation  
- Efficient communication between LANs  
- Scalable for future expansion  

---

# Comparison of RIP and OSPF (Based on Simulation)

## 1. Convergence Time

- RIP exchanges updates periodically, so convergence is slower.
- OSPF shares link-state information immediately after changes.

**Conclusion:** OSPF converges faster than RIP.

---

## 2. Routing Metric

- RIP uses **Hop Count** as metric.
- OSPF uses **Cost based on bandwidth**.

**Conclusion:** OSPF selects better and more optimal routes.

---

## 3. Efficiency

- RIP sends complete routing tables periodically.
- OSPF sends updates only when changes occur.

**Conclusion:** OSPF is more bandwidth efficient.

---

## 4. Scalability

- RIP is suitable for small networks.
- OSPF supports large and complex enterprise networks.

**Conclusion:** OSPF is more scalable than RIP.

---

# Final Conclusion

From the simulation results, it is concluded that **OSPF performs better than RIP** in terms of:

- Faster convergence  
- Better route selection  
- Higher efficiency  
- Greater scalability  

RIP is easier to configure and suitable for small networks, while OSPF is preferred for medium and large networks.
