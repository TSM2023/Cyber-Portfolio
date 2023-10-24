# Wireshark Lab

## Overview
Configuring Wireshark for Traffic Analysis

## Getting Started

### Utilities Used

* Oracle VM VirtualBox
* Kali Linux
  
### Installation & Execution 

* To download Wireshark in Kali Linux, open the CLI and input: 
```
sudo apt install Wireshark
```
* Once installed, input **Wireshark** into the CLI
```
Wireshark
```

   <b>OR</b> 


* In the searchbar of Kali Linux, type in **Wireshark**

![image](https://github.com/T-A-Smith/Wireshark-Practice/assets/143060189/2a23e156-cf3d-435a-8356-45b57c09bdd5)


<br>

*  On the "Welcome to Wireshark" page, double click on **eth0** interface
  
![image](https://github.com/T-A-Smith/Wireshark-Practice/assets/143060189/697eef59-5de6-4e0b-af34-e876589de602)


<br>

* Click on 🟥 to stop capturing packets

![image](https://github.com/T-A-Smith/Wireshark-Practice/assets/143060189/2de0a561-10b1-43b8-98fa-1b7cc2797bc9)



<br>


* Select Edit > Configuration Profiles... 

![image](https://github.com/T-A-Smith/Wireshark-Practice/assets/143060189/c340f699-fd79-4eda-85d7-680b8de2bd34)


<br>

* Select **Default** > click on **Copy this Profile** ( looks like two little boxes ) > then rename. 
* I renamed mine UPDATED. The **Type** will show as **Personal.**
  
![image](https://github.com/T-A-Smith/Wireshark-Practice/assets/143060189/bfe09672-85a9-45b1-8c26-c5dda91adf90)




![image](https://github.com/T-A-Smith/Wireshark-Practice/assets/143060189/6d20acae-054d-47f9-a43e-ef0fdbb2f62d)

<br>

* Next, go to **EDIT** tab > **PREFERENCES...**
  

  ![image](https://github.com/T-A-Smith/Wireshark-Practice/assets/143060189/ea23e903-1dfc-4733-bf53-5334d6d1400b)


<br>

* Under Appearance, select **COLUMNS**
* Select - to remove protocol, length, and number of columns <br>
* Select + to add: <br>
  -Add (+) TITLE: Src Port TYPE: Src port (unresolved) <br>
  -Add (+) TITLE: Dest Port TYPE: Dest port (unresolved) <br>
  Rearrange as shown in photo

![image](https://github.com/T-A-Smith/Wireshark-Practice/assets/143060189/a29cb2de-05b1-4b7a-8d8b-cd273ca0c87f)

<br>

* When using Wireshark to look at HTTP traffic, it is extremely useful to apply a display filter so that we're only seeing HTTP requests.
* Click on **Apply a display filter** and type in **http.request**

   <br>
![image](https://github.com/T-A-Smith/Wireshark-Practice/assets/143060189/a659ac9f-a69d-4fa2-9cd0-fd359f85c04c)

![image](https://github.com/T-A-Smith/Wireshark-Practice/assets/143060189/680bfa35-0495-420b-b82d-e051317c7d09)

<br>

* Expand the breakout in the middle section, so you see the **Host:** line in the HTTP header.  Right-click on **Host:** and select "Apply as Column" from the menu.


![image](https://github.com/T-A-Smith/Wireshark-Practice/assets/143060189/75656451-9f83-46a5-a10a-b48eb37415a4)


