![opencti](https://github.com/user-attachments/assets/7b3c2069-7f1d-4461-82eb-f64edae21120)
# CTI-Integration

## Objective

In this detection lab, the goal is to use an open-source Threat Intelligence platform to centralize all of my CTI data. This helps me correlate observables such as domains, IP addresses, or file hashes in one place, and potentially find more information that helps me understandthe the flow of data and how different threat indicators are connected.In this project, I set up OpenCTI and integrated it with Splunk. I also created a custom CTI feed using data from OTX AlienVault.

### Skills Learned

- Deployed Ubuntu server and integrated it with `OpenCTI` and `Splunk` for centralized threat intelligence management.
- Used `GitHub` to manage code and integrated it into `Docker Compose` (YAML) for automated deployment.
- Learned to deploy and manage applications using `Docker containers`
- Connecting and integrating `AlienVault` OTX with security platforms via API.
- Developed and managed `CTI feeds` for threat intelligence integration.
- Enhanced critical thinking, problem-solving, and troubleshooting abilities during lab design projects.

### Tools Used

- OpenCTI - Threat Intelligence Platform
- Docker -  for packaging, distributing, and running applications in isolated environments
- Splunk - (SIEM) 
- Github
- AlienVault OTX - Platform to collect and share threat intelligence data.

---

## Steps

#### 1.Setup OpenCTI

-Ubuntu Server installation in VirtualMachine and SSH connection via PowerShell
![111111111111111](https://github.com/user-attachments/assets/c003de98-949c-44cc-9493-c4891cc31e2b)

-After installing `Docker` and `OpenCTI` -> `sudo apt-get install docker-compose` . Once Docker is installed, we clone the repository.

git clone - > `https://docs.opencti.io/latest/deployment/installation/#using-docker`
![33333333333333333](https://github.com/user-attachments/assets/030531f4-e39b-4af1-ae36-83a61f65eba5)

-This file contain all the configuration that `Docker` will reference
![4444444444444](https://github.com/user-attachments/assets/2aff33d8-851c-471d-bf6a-6bb23efff8f5)





