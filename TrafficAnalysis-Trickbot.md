# ⚠️IN PROGRESS⚠️

 
  # Malware Traffic Analysis - TRICKBOT
  
 <p align="center">

   ![image](https://github.com/T-A-Smith/Wireshark-Practice/assets/143060189/a5fc7dcc-8b00-47c1-89ec-111d7c84e51c)
 </p>

## Trickbot Overview

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

  


  



