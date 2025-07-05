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
- UUID Generator
---

## Steps Taken

#### 1.Setup OpenCTI

-Ubuntu Server installation in VirtualMachine and SSH connection via PowerShell
![111111111111111](https://github.com/user-attachments/assets/c003de98-949c-44cc-9493-c4891cc31e2b)


git clone - > `https://docs.opencti.io/latest/deployment/installation/#using-docker`

-This file contain all the configuration that `Docker` will reference
![4444444444444](https://github.com/user-attachments/assets/2aff33d8-851c-471d-bf6a-6bb23efff8f5)

-There is a hidden file named .env.sample which contains variables intended to be pulled into docker-compose.yml.
For the admin token, generate a `UUID` from https://www.uuidgenerator.net/. The fields I have modified are marked.

![env](https://github.com/user-attachments/assets/0b630835-2e07-4407-ba06-18efdb74f6d6)


-All configuration are done and start docker -> `systemctl start docker.service /start docker` and `sudo docker-compose up -d`
 Then we have access to `OpenCTI`

![dashboard](https://github.com/user-attachments/assets/b858246c-3f40-4af2-ba14-6a25de1a82cc)


-Next thing to do is what are calling `EXTERNAL CONNECTORS` which are third party Websites that can integrade with OpenCTI to provide additional capabilitie. `OTX AlienVault` You have to create an account.


OpenCTI External Connectors -> `https://github.com/OpenCTI-Platform/connectors/tree/master/external-import`

![Screenshot 2025-07-05 102354](https://github.com/user-attachments/assets/e803bbf9-4c12-40c8-a7c7-850ba05188fa)


#### 2.Integrating Splunk

-The first step in integrating Splunk with OpenCTI is to create an external connector and KV
![SPLUNK (2)](https://github.com/user-attachments/assets/7dd65bd9-c223-4a7b-befc-8d4637db2968)

-Go over to our `Splunk`
![splunkkkk](https://github.com/user-attachments/assets/d9f638b1-1dda-45a9-b7fe-53fb1b163b0c)

-`External connectors` are integrated
 ![ingest](https://github.com/user-attachments/assets/ab3632bf-dc92-4310-975d-42fa98788438)


 #### 3. Creating CSV Feed

-Data -> Data Sharing ->  CSV Feeds
![111](https://github.com/user-attachments/assets/da029336-7985-4313-89a5-b3cf5fa983ff)

-My CTI Feed

![ctifeed](https://github.com/user-attachments/assets/87c0abbe-2435-4a7c-b2ef-1fd778fc57c2)

-Full list of all the `domains` that are within in CTI platform.

![Screenshot 2025-07-05 115611](https://github.com/user-attachments/assets/4cd90d28-419d-42c7-aad9-8930602969f3)

---

### Summary

`OpenCTI` provides you and the analyst team with the capability to gather more information about threats observed in your environment all within a single tool.
