## Automated ELK Stack Deployment

The files in this repository were used to configure the network depicted below.

![Diagram](Images/Cloud_Infrastructure_Diagram.png)

These files have been tested and used to generate a live ELK deployment on Azure. They can be used to either recreate the entire deployment pictured above. Alternatively, select portions of the .yml file may be used to install only certain pieces of it, such as Filebeat.

* The ansible-playbooks [Elk.yml](Ansible-Playbooks/Install-ELK). and [filebeat.yml](Ansible-Playbooks/Filebeat-playbook.yml) are needed to create and implement the Elk-Server.

This document contains the following details:
* Description of the Topologu
* Access Policies
* ELK Configuration
* Beats in Use
* Machines Being Monitored
* How to Use the Ansible Build


### Description of the Topology

The main purpose of this network is to expose a load-balanced and monitored instance of DVWA, the D*mn Vulnerable Web Application.
Load balancing ensures that the application will be highly available, in addition to restricting access to the network.

* What aspect of security do load balancers protect?.
Load Balancing contributes to the Availability aspect of security in regards to the CIA Triad.

* What is the advantage of a jump box?.
The advantage of a JumpBox is the orgination point for launching Administrative Tasks. This ultimately sets the JumpBox as a SAW (Secure Admin Workstation). All Administrators when conducting any Administrative Task will be required to connect to the JumpBox (SAW) before perfoming any task/assignment. 

Integrating an ELK server allows users to easily monitor the vulnerable VMs for changes to the logs and system traffic.
* What does Filebeat watch for? 
Filebeat watches for log files/locations and collects log events.

* What does Metricbeat record?
Metricbeat records metric and statistical data from the operating system and from services running on the server.

The configuration details of each machine may be found below.


|    Name    | IP Address |      Function     |   Operating Sistem   |
|:----------:|:----------:|:-----------------:|:--------------------:|
| Web1       | 10.0.0.8   | docker - DVWA     | linux (ubuntu 18.04) |
| Web2       | 10.0.0.7   | docker - DVWA     | linux (ubuntu 18.04) |
| Jump-box   | 10.0.0.4   | gateway - ansible | linux (ubuntu 18.04) |
| ELK-server | 10.1.0.4   | ELK               | linux (ubuntu 18.04) |

### Access Policies

The machines on the internal network are not exposed to the public Internet. 

Only the Jump-box machine can accept connections from the Internet. Access to this machine is only allowed from the following IP addresses:
Personal IP address

Machines within the network can only be accessed by ssh.

The only machine that is able to connect to the Elk-Server (10.1.0.4) is via JumpBox from Private IP (10.0.0.4)
A summary of the access policies in place can be found in the table below.

|   Name   | Publicly Accessible |  Allowed IP Addresses  |
|:--------:|:-------------------:|:----------------------:|
| Jump-box |          no         | Personal IP only       |
| Web-1    |          no         | 10.0.0.4               |
| Web-2    |          no         | 10.0.0.4               |
| ELK      |          no         | 10.0.0.4 & Personal IP |

### Elk Configuration

Ansible was used to automate configuration of the ELK machine. No configuration was performed manually, which is advantageous because...
- _TODO: What is the main advantage of automating configuration with Ansible?_

The playbook implements the following tasks:
- _TODO: In 3-5 bullets, explain the steps of the ELK installation play. E.g., install Docker; download image; etc._
- ...
- ...

The following screenshot displays the result of running `docker ps` after successfully configuring the ELK instance.

![TODO: Update the path with the name of your screenshot of docker ps output](Images/docker_ps_output.png)

### Target Machines & Beats
This ELK server is configured to monitor the following machines:
- _TODO: List the IP addresses of the machines you are monitoring_

We have installed the following Beats on these machines:
- _TODO: Specify which Beats you successfully installed_

These Beats allow us to collect the following information from each machine:
- _TODO: In 1-2 sentences, explain what kind of data each beat collects, and provide 1 example of what you expect to see. E.g., `Winlogbeat` collects Windows logs, which we use to track user logon events, etc._

### Using the Playbook
In order to use the playbook, you will need to have an Ansible control node already configured. Assuming you have such a control node provisioned: 

SSH into the control node and follow the steps below:
- Copy the _____ file to _____.
- Update the _____ file to include...
- Run the playbook, and navigate to ____ to check that the installation worked as expected.

_TODO: Answer the following questions to fill in the blanks:_
- _Which file is the playbook? Where do you copy it?_
- _Which file do you update to make Ansible run the playbook on a specific machine? How do I specify which machine to install the ELK server on versus which to install Filebeat on?_
- _Which URL do you navigate to in order to check that the ELK server is running?

_As a **Bonus**, provide the specific commands the user will need to run to download the playbook, update the files, etc._
