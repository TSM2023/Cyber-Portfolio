# Wireshark Lab

Simple overview of use/purpose. Malware Traffic Analysis; installation and configuration,

## Description
In this lab,
An in-depth paragraph about your project and overview of use.

## Getting Started

### Utilities Used

* Kali Linux

### Installing
To download Wireshark in Kali Linux, open the CLI and type in 

**sudo apt install Wireshark**

![WS_Download](https://github.com/T-A-Smith/Wireshark-Lab/assets/143060189/8899afc5-d29c-4982-b3f7-d8a6fb5fe7f2)

Type in **y** when asked Do you want to continue?

Check version wireshark -v (Latest version 4.08)
![WS_Version](https://github.com/T-A-Smith/Wireshark-Practice/assets/143060189/b2c8361d-21ab-41bd-81fa-271718e7ea77)


* How/where to download your program
* Any modifications needed to be made to files/folders

### Executing program

* How to run the program...Installation and Configuration for Traffic Analysis
* Step-by-step bullets

To start, type Wireshark into CLI
![image](https://github.com/T-A-Smith/Wireshark-Lab/assets/143060189/09cf941d-7fa3-4e02-9228-4fcfaddc4dd5)

Welcome page
Double click on eth0 interface
![image](https://github.com/T-A-Smith/Wireshark-Practice/assets/143060189/a8fe51dd-ee57-4762-a7d5-28d10e927fc5)

Packets being captured
![image](https://github.com/T-A-Smith/Wireshark-Practice/assets/143060189/ab9d0fd6-a61b-4951-b4ef-609b666b18cb)

Open settings/enable promiscuous mode on all interfaces
![image](https://github.com/T-A-Smith/Wireshark-Practice/assets/143060189/f342b5e2-4557-4b84-b328-45d5a6636d15)


Ensure the following options are checked

![image](https://github.com/T-A-Smith/Wireshark-Practice/assets/143060189/2733d99e-4690-4abc-9589-6e3ce7a58c33)

Edit > Preferences
In the columns tab, add Source Port and Destination Port. ...(continue to edit) type - dst port (unresolved) src port (unresolved)

![image](https://github.com/T-A-Smith/Wireshark-Practice/assets/143060189/e8e6e597-553b-429c-8aff-47033d1a4936)



## Help

Any advise for common problems or issues.
```
command to run if program contains helper info
```

## Authors

Contributors names and contact info



## Version History

* 0.2
    * Various bug fixes and optimizations
    * See [commit change]() or See [release history]()
* 0.1
    * Initial Release
