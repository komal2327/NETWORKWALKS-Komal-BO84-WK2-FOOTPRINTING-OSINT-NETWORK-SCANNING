# NETWORKWALKS-Komal-BO84-WK2-FOOTPRINTING-OSINT-NETWORK-SCANNING
This repository contains my Week 2 practical work focused on Information Gathering, Open-Source Intelligence (OSINT), Footprinting, and Network Discovery using Kali Linux.

# Week 2 – Footprinting, OSINT & Network Scanning

## Cybersecurity Internship | Practical Lab Submission

The exercises provided hands-on experience with two important cybersecurity tools: **theHarvester** and **Zenmap (Nmap)**.

---

## Objectives

- Understand the fundamentals of footprinting and reconnaissance.
- Gather publicly available email addresses and subdomains using theHarvester.
- Explore different OSINT data sources.
- Understand IP addressing and CIDR notation.
- Identify active hosts within a local network using Nmap and Zenmap.
- Gain practical experience with reconnaissance tools in Kali Linux.

## Tools & Technologies

| Tool | Purpose |
|---|---|
| Kali Linux | Penetration testing environment |
| theHarvester | OSINT and information gathering |
| Baidu | Public search engine data source |
| Zenmap | Graphical interface for Nmap |
| Nmap | Network discovery and scanning |
| Terminal | Executing Linux commands |

---

# Task 1 – OSINT & Footprinting Using theHarvester

### Objective

To identify publicly available email addresses and subdomains associated with the target organization `microsoft.com` using theHarvester in Kali Linux.

### Background

theHarvester is an open-source reconnaissance tool used to collect publicly available information from search engines, public databases, and other supported sources.

It can help identify:

- Email addresses
- Subdomains
- Hostnames
- Employee names (where publicly indexed)
- Other publicly available organizational information

### Exercise 1: Information Gathering Using Baidu

**Target:** `microsoft.com`

**Data Source:** Baidu

**Maximum Results:** 1000

**Command:**

```bash
theHarvester -d microsoft.com -b baidu -l 1000
```

**Procedure:**

1. Open the Kali Linux terminal.
2. Execute theHarvester command.
3. Specify `microsoft.com` as the target domain.
4. Select Baidu as the information source.
5. Set the maximum result limit to 1000.
6. Review the collected email addresses, subdomains, and host information.

**Screenshot:**
<img width="1613" height="927" alt="Screenshot 2026-11-13 005810" src="https://github.com/user-attachments/assets/c526285d-6a4d-4aa2-9455-f9e9e6a61584" />



### Exercise 2: Information Gathering Using All Sources

**Target:** `microsoft.com`

**Data Sources:** All supported sources (`all`)

**Maximum Results:** 50

**Command:**

```bash
theHarvester -d microsoft.com -b all -l 50
```

**Procedure:**

1. Execute theHarvester in Kali Linux.
2. Specify the target domain.
3. Select all supported data sources.
4. Configure the result limit to 50.
5. Examine and compare the collected information.

**Screenshot:**

<img width="1920" height="922" alt="Screenshot_2026-11-13_02_21_53" src="https://github.com/user-attachments/assets/44842587-4b94-4e96-9c5b-d29534a29bd7" />


### Key Learning Outcomes

- Understanding OSINT-based reconnaissance.
- Learning how to use search engines as information sources.
- Identifying publicly indexed organizational information.
- Understanding domain and subdomain enumeration.

---

# Task 2 – Network Discovery Using Zenmap & Nmap

### Objective

To identify active devices within my own local network using network discovery techniques.

### Step 1: Identify Network Configuration

**Command:**

```bash
ifconfig
```

**Purpose:**

- Identify active network interfaces.
- Find the assigned IPv4 address.
- Understand the network configuration.
- Determine the appropriate subnet for scanning.

**Screenshot:**

<img width="1077" height="773" alt="Screenshot 2026-11-13 014910" src="https://github.com/user-attachments/assets/8e58b16d-3af7-4ada-b88b-ab2322554c71" />


### Step 2: Test Network Connectivity

**Command:**

```bash
ping <target-IP>
```

**Example:**

```bash
ping 192.168.1.1
```

**Purpose:**

- Verify network connectivity.
- Check whether the target responds to ICMP echo requests.
- Understand basic network troubleshooting.



### Step 3: Perform Network Discovery Scan

**Command:**

```bash
nmap -sn <your-network-IP>/24
```

**Example:**

```bash
nmap -sn 192.168.1.0/24
```

**Purpose:**

- Discover active hosts within the specified subnet.
- Identify devices responding to host discovery probes.
- Understand the basics of network reconnaissance.

The `-sn` option performs host discovery without conducting a port scan.

**Screenshot:**

<img width="973" height="598" alt="image" src="https://github.com/user-attachments/assets/e49c99f5-61d3-4ef1-8164-d4f42ac058d0" />


### Step 4: Explore Zenmap

Zenmap provides a graphical interface for Nmap, making network scanning results easier to understand and visualize.

**Activities:**

- Configure the target network.
- Execute a host discovery scan.
- Review discovered hosts.
- Explore scan results and network topology visualization.

**Screenshot:**

<img width="972" height="586" alt="image" src="https://github.com/user-attachments/assets/779a2a77-aaba-49b5-afef-637200863116" />


### Key Learning Outcomes

- Understanding IP addresses and subnetting.
- Learning the fundamentals of CIDR notation.
- Performing basic network connectivity tests.
- Discovering active hosts using Nmap.
- Understanding graphical network scanning through Zenmap.

---

## Overall Learning Outcomes

Through these practical exercises, I gained experience in:

1. Performing OSINT-based information gathering.
2. Using theHarvester for email and subdomain enumeration.
3. Exploring multiple publicly available information sources.
4. Understanding local network configuration.
5. Performing host discovery using Nmap.
6. Exploring network scanning results through Zenmap.

---

## Repository Structure

```text
WEEK2-FOOTPRINTING-OSINT-NETWORK-SCANNING/
│
├── README.md
│
├── Task-1-theHarvester/
│   ├── README.md
│   └── screenshots/
│       ├── baidu-scan.png
│       └── all-sources-scan.png
│
└── Task-2-Zenmap/
    ├── README.md
    └── screenshots/
        ├── ifconfig.png
        ├── ping-test.png
        └── network-scan.png
```

---

## Conclusion

Week 2 provided valuable hands-on experience with reconnaissance and network discovery techniques. Working with theHarvester helped me understand how publicly available information can be collected during the footprinting phase, while Nmap and Zenmap introduced me to practical network discovery and host identification.

These exercises strengthened my understanding of the initial stages of ethical hacking and cybersecurity assessments.

---

## Disclaimer

This repository is intended strictly for educational purposes and authorized cybersecurity learning.

The OSINT exercise uses publicly available information associated with the specified domain. Network discovery activities should only be performed on networks and systems owned by you or for which you have explicit permission.

**Learning | Practicing | Improving | Securing**

#Cybersecurity #EthicalHacking #OSINT #KaliLinux #theHarvester #Zenmap #Nmap
