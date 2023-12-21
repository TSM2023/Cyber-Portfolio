# ⚠️IN PROGRESS⚠️

 
  # Malware Traffic Analysis 
  
 <p align="center">

   ![image](https://github.com/T-A-Smith/Wireshark-Practice/assets/143060189/a5fc7dcc-8b00-47c1-89ec-111d7c84e51c)
 </p>

## Overview
* Below is the process I used to analyze a pcap file consisting of network traffic with TrickBot malware
* Trickbot Information:
  - Information stealing and banking malware
  - Distributed through embedded URLs, infectected attachemnts in malspam, or other malware (ie. Emotet malware can distribute TrickBot)
  - Common indicators:
     - HTTPS/SSL/TLS traffic over TCP ports 447 and 449 (unusual)
     - HTTP requests contain png (Windows exe files may masquerade as png)
     - Frame contains “This program cannot be run in DOS mode" (often seen in exe files)
     - HTTP traffic over TCP port 8082 (sends sensitive information from the infected host like passwords to C2 servers)
 

## Analyzing a Trickbot Infection

* File > Open > Navigate to saved PCAP file

<br>

![image](https://github.com/T-A-Smith/Wireshark-Practice/assets/143060189/0c5c5f77-2517-4254-bce2-fe29069d18ea)

<br>

* To filter traffic, type **http.request** in the **Apply a display filter** textbox
  
**BEFORE FILTER** 
![image](https://github.com/T-A-Smith/Wireshark-Practice/assets/143060189/ff5440b3-2c44-492d-bf83-2218cdccc3bd)

**AFTER FILTER**
![image](https://github.com/T-A-Smith/Wireshark-Practice/assets/143060189/dcbba400-4f24-4dd3-8ed6-ef3d999c0471)

<br> 

* After filtering the traffic, go to **File > Export Objects > HTTP...** to export objects/files from the pcap for analysis

  ![image](https://github.com/T-A-Smith/Wireshark-Practice/assets/143060189/bf3f249f-20b7-4afa-a9f5-c579f7f5472e)

<br> 

* Next, I want to analyze content types, so I sort alphabetically by clicking on **Content Type**  
  
  ![image](https://github.com/T-A-Smith/Wireshark-Practice/assets/143060189/c7279df9-2a15-4e92-a105-c913142b736a)

<br> 

* Malware is typically downloaded via attachements. When exporting files, I look for suspicious content types, which usually start with *application/*
* For example, malicious scripts can be embedded in PDF files, so when looking for suspicious content types, I'd look for *application/pdf* and export it for further analysis
* Looking at the alphabetically ordered content type, there are 3 that begin with *application/* that probably require further analysis

![image](https://github.com/T-A-Smith/Wireshark-Practice/assets/143060189/b9fc73b5-aaa5-4be6-8f77-7b6badac0601)

<br> 

* Select/highlight the content to download, then **SAVE**

  ![image](https://github.com/T-A-Smith/Wireshark-Practice/assets/143060189/555813f1-0db6-43ca-b47e-a5304b02b4c5)

  
<br>

* On the next screen, choose the location where you would like to save the files, then click **SAVE**

![image](https://github.com/T-A-Smith/Wireshark-Practice/assets/143060189/b0a084a8-0e05-4b29-891b-0bd277362705)

<br> 

* Once saved, we can extract the hashes of the files
* To do this, open up a command terminal window and type in md5sum followed by the file path of the file. Press **ENTER**

  ![image](https://github.com/T-A-Smith/Wireshark-Practice/assets/143060189/cf253588-c2b8-4905-8737-34ff7da9bdfc)

![image](https://github.com/T-A-Smith/Wireshark-Practice/assets/143060189/da041b3d-9b38-4de6-8481-3083ff5995ff)

* In a web browser,  navigate to VirusTotal.com. Select the SEARCH tab and input the hash value in the search bar
  
![image](https://github.com/T-A-Smith/Wireshark-Practice/assets/143060189/73df8330-205f-4b34-ba0e-8438148ee73f)

**OR**

* Drag and drop the suspicious file
  
![image](https://github.com/T-A-Smith/Wireshark-Practice/assets/143060189/a98f2241-8f54-4dee-ad58-d19a55eed39c)

 * Repeat for each file
 * Results: 
   
    -*application/octet-stream*
   
   ![image](https://github.com/T-A-Smith/Wireshark-Practice/assets/143060189/b69ecb9a-0f89-4736-b9d7-493e3bb18ceb)

<br>

   -*application/zip* 
 ![image](https://github.com/T-A-Smith/Wireshark-Practice/assets/143060189/32a30cf7-429d-4572-a18f-dd710c5bb554)

<br>

  -*application/vnd.ms-cab-compressed* 
![image](https://github.com/T-A-Smith/Wireshark-Practice/assets/143060189/365fb4a7-252e-4149-ab8f-cb732335cf6c)


* 	Based on VirusTotal, two of the files submitted are considered malicious
    - Application/zip
    - Application/octet-stream
 
* Next, it's time to examine HTTP/HTTPS traffic and look for specific behaviors indicating this is a TrickBot infection





