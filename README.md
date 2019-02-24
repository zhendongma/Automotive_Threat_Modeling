# Automotive Threat Modeling
A repository for templates and things related to automotive threat modeling

## Background
If you have done threat modeling and used the [Microsoft Threat Modeling Tool (MSTMT)](https://www.microsoft.com/en-us/securityengineering/sdl/threatmodeling), you would know how much a good template can help you and your team to conduct threat enumeration. A large part of automotive threat modeling could be automated if templates are created and shared among the security engineers. Until now, the [automotive template](https://github.com/nccgroup/The_Automotive_Threat_Modeling_Template) from NCC Group is often used. But it seems to be skewed toward ADAS system, and there are many false-positives in threat generation. 

This template is created to encode the threat catalog from the [UN Task Force on Cyber security and OTA issues (CS/OTA)](https://wiki.unece.org/pages/viewpage.action?pageId=40829521). The CS/OTA cybersecurity threat [table](https://wiki.unece.org/download/attachments/44269802/TFCS-05-05-Rev2%20%28Chair%29%20Table%20on%20CS%20threats%20-%20with%20explanations%20and%20draft%20definitions.xlsx?api=v2) has a good description of the threats related to automotive OTA update. To my opinion, it is more intuitive and self-explanatory for high-level automotive threat modeling. This template encodes the threats from the CS/OTA table as-is. I have made several necessary extensions when converting it to a MSTMT template. 

* Stencils. Most stencils in the template are directly taken from the CS/OTA table. Some stencil names are slightly modified to comply with the MSTMT rules. A few stencils are added for common automotive components. Other stencil information from the CS/OTA table is added as stencil properties.
* Threat types. Not all threats in the CS/OTA table are categorized according to STRIDE. Missing STRIDE categories are added.   
* Threat properties. Each threat in the CS/OTA table has some additional information. These information are added as threat properties. The explanation can be found in the CS/OTA table.  
* Threat generation expressions. Threat generation expressions are added based on my analysis and interpretation of each of the threats in the CS/OTA table. The goal is minimize false-positive and false-negative when MSTMT automatically generates applicable threats.  

## Installation
Download the tb7 file. Run Microsoft Threat Modeling Tool 2016. If you just want to use the template, choose it under "Template For New Models". If you want to modify or add your own stencils and threat types, choose it under "Open Template". 

You can also merge this template with other templates to increase your threat repository.

## Usage
A few things to know before you start:
* Use existing stencils if possible. If not, use the "generic" ones instead. You can always change the "Name" of a stencil to suit your need. It does not effect threat generation.
* Place trust boundaries. 
* Create different threat models for different use cases/scenarios.
* Note that automatically generated threats are just a starting point. The resulting list is not exhaustive, but it gives you a good start for further enumeration. 
* You probably need to review and delete irrelevant threats. Note that the same threats can be seen on different processes and data flows. 

## Disclaimer
This automotive threat modeling template contains publicly available threat information and is offered "as-is", without warranty. It was created in my personal capacity and reflects my own opinion.

## Feedback
If you like the template or want to improve it, send me an email dr.zhendong.ma [at] gmail [dot] com
