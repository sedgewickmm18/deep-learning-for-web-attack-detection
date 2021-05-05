## Machine Learning for Web Attack Detection

### Introduction

Web-based vulnerabilities represent a substantial portion of the security exposures of computer networks. In order to detect known web-based attacks,
misuse detection systems are equipped with a large number of signatures. Unfortunately, it is difficult to keep up with the daily disclosure of web-related
vulnerabilities, and, in addition, vulnerabilities may be introduced by installation-specific web-based applications. Therefore, misuse detection systems 
should be complemented with anomaly detection systems. A service will be provided where by applying end-to-end deep learning we will detect cyber-attacks
autonomically in real-time and adapt efficiently, scalably, and securely to thwart them.

### Goals

Our goal is to build a web attack detector that makes use of machine learning

* The machine learning approach will be based on a call stack recorder similar to the Robust Software Modeling Tool
[RMST](https://www.researchgate.net/publication/318578126_A_Feasibility_Study_of_Autonomically_Detecting_In-Process_Cyber-Attacks). It detects call sequences
that are highly unlikely.
* Inference: When a client sends a request to a web-applicaton the agent will record a trace and the trained model will encode and decode the recontruction error.
If reconstruction error is larger than the learned threshold it will be classified as an attack otherwise it will be a normal request.
* Training: The model will be build based on stack trace recording during regular operation.
* Validation: The model will be validated with specific web attack vectors like [this](https://github.com/foospidy/payloads)
* An agent server component will be there which will address the problem of mapping task/application-level abstractions to physical computing resources. We propose 
to build the solution on QRadar as a typical product in the security information and event management (SIEM) space. This allows to limit the efforts put into a UI.

### Overview

![image](https://github.com/sedgewickmm18/deep-learning-for-web-attack-detection/blob/main/images/WebAttack.png)
