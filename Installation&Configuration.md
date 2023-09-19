# Wireshark Lab

## Overview
How I install and configure Wireshark for Malware Traffic Analysis

## Getting Started

### Utilities Used

* Kali Linux
  
### Installing
* To download Wireshark in Kali Linux, open the CLI and input:
```
sudo apt install Wireshark
```


![WS_Download](https://github.com/T-A-Smith/Wireshark-Lab/assets/143060189/8899afc5-d29c-4982-b3f7-d8a6fb5fe7f2) 


* To continue the installation, input **Y** and press **ENTER**: 

<br>

* Check the version of Wireshark to ensure version 3.6.2 or later has been installed (Latest version 4.08) 
```
Wireshark -v
```

![WS_Version](https://github.com/T-A-Smith/Wireshark-Practice/assets/143060189/b2c8361d-21ab-41bd-81fa-271718e7ea77)

<br>

 ### Executing Program

* To start, input **Wireshark** into the CLI
```
Wireshark
```

![image](https://github.com/T-A-Smith/Wireshark-Practice/assets/143060189/7d41fd49-86d6-4701-90c8-ec1a31ca13e6) 

<br>


* On the "Welcome to Wireshark" page, double click on **eth0** interface
![image](https://github.com/T-A-Smith/Wireshark-Practice/assets/143060189/a8fe51dd-ee57-4762-a7d5-28d10e927fc5) 

<br>

* *Example of packets being captured after clicking on eth0:*
![image](https://github.com/T-A-Smith/Wireshark-Practice/assets/143060189/ab9d0fd6-a61b-4951-b4ef-609b666b18cb)

<br>


* **Settings** > INPUT tab > Enable promiscuous mode on all interfaces
<br>

![image](https://github.com/T-A-Smith/Wireshark-Practice/assets/143060189/f342b5e2-4557-4b84-b328-45d5a6636d15)

<br>

* **Settings** > OPTIONS tab, **Select:** <br>
- [x] *Update list of packets in real-time*
- [x] *Automatically scroll during live capture*
- [x] *Resolve MAC addresses*


![image](https://github.com/T-A-Smith/Wireshark-Practice/assets/143060189/2733d99e-4690-4abc-9589-6e3ce7a58c33)

<br>

* **Edit** > Preferences > Columns <br>
    - Add (+) TITLE: Source Port  TYPE: Src port (unresolved) <br>
    - Add (+) TITLE: Destination Port TYPE: Dest port (unresolved) <br>
    - Press OK

 <br>
 
![image](https://github.com/T-A-Smith/Wireshark-Practice/assets/143060189/e8e6e597-553b-429c-8aff-47033d1a4936)




