# ansible-jenkins
Agenda: Create your pipeline with Jenkins &amp; Ansible Config tool. 


### Create a declarative pipeline with Jenkins/Ansible (Inventory/Playbook) - Agenda

- Setup your jenkins server
- Prepare a docker image e.g. Apache/webserver
- Now write inventory/playbook to build docker image and up apache webserver
- Now your will see a Hello Ansible


### Steps
- Install Java-JDK, Jenkins, Ansible, Docker, Git - in ONE VM (lets name it as Jenkins-Ansible-VM)
 > Sometimes you may be face troubleshooting in Jenkins/Ansible specially if you are using RedHat ansible should be registered from subscription-manager 
 
 > Ansible can install in other OS like Centos/Ubuntu/Amazon Linux easily. Also make sure you have installed JAVA-JDK before jenkins
- Once installation done - start jenkins server on your port 8080 (default)
- Once account setup done, install jenkins plugin here and configure it accordingly - i.e you can point jenkins path e.g. /usr/bin, INV file name e.g. hosts.inv, playbook file name
- Then create a new job by choosing pipeline option
- Point this repository under source control 
- Build with shell - commands 
- The pipeline script in shell commands are given here in "Jenkinsfile" 
- If you want to configure auto checkout repo-to-jenkins then mark "GIT SCM Polling" as checked
- Build now 
- You can see the pipeline actions now
- If stages are success then check the web URL (your target VM box IP/domain) e.g. 10.1.1.1 or domain.com


#### Additional 
- When you executing ansible playbook in pipeline it will ask you to connect target machine/groups SSH connection. So create SSH (jenkins credentials) 
> Goto jenkins credentials => Choose SSH username with private option then fill the options accordingly

> Here you may need to execute from target machine "ssh-keygen"  for public/private key. Once generate the key copy and paste to jenkins (at credentials part)

> Disable HOST  SSH key checkin (if you are using spinnet generator area/for ansible)
