# Wireshark Lab

## Overview
How I install and configure Wireshark for Malware Traffic Analysis

## Getting Started

### Utilities Used

* Kali Linux

### Installing
To download Wireshark in Kali Linux, open the CLI and input:
```
sudo apt install Wireshark
```


![WS_Download](https://github.com/T-A-Smith/Wireshark-Lab/assets/143060189/8899afc5-d29c-4982-b3f7-d8a6fb5fe7f2)

To continue the installation, input **Y** and press **ENTER**: 


Next, check the version of Wireshark to ensure version 3.6.2 or later has been installed (Latest version 4.08) 
```
Wireshark -v
```

![WS_Version](https://github.com/T-A-Smith/Wireshark-Practice/assets/143060189/b2c8361d-21ab-41bd-81fa-271718e7ea77)


### Executing program

To start Wireshark, input **Wireshark** into the CLI
```
Wireshark
```

![image](https://github.com/T-A-Smith/Wireshark-Practice/assets/143060189/c63e9eda-b0cf-4e89-b962-37c88b658c45)


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

```

## Authors

Contributors names and contact info



## Version History

* 0.2
    * Various bug fixes and optimizations
    * See [commit change]() or See [release history]()
* 0.1
    * Initial Release
