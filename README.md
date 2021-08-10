# ansible-jenkins
Agenda: Create your pipeline with Jenkins &amp; Ansible Config tool. 


### Create a declarative pipeline with Jenkins/Ansible (Inventory/Playbook) - Agenda

- Setup your jenkins server
- Prepare a docker image e.g. Apache/webserver
- Now write inventory/playbook to build docker image and up apache webserver
- Now your will see a Hello Ansible


### Steps
- Install Java-JDK, Jenkins, Ansible, Docker - in ONE VM (lets name it as Jenkins-Ansible-VM)
 > Sometimes you may be face troubleshooting in Jenkins/Ansible specially if you are using RedHat ansible should be registered from subscription-manager 
 
 > Ansible can install in other OS like Centos/Ubuntu/Amazon Linux easily. Also make sure you have installed JAVA-JDK before jenkins
- Once installation done - start jenkins server on your port 8080 (default)
- Then create a new job by choosing pipeline option
- Point this repository under source control 
- Build with shell - commands 
- The pipeline script in shell commands are given here in "Jenkinsfile" 
- If you want to configure auto checkout repo-to-jenkins then mark "GIT SCM Polling" as checked
- Build now 
- You can see the pipeline actions now
- If stages are success then check the web URL (your target VM box IP/domain) e.g. 10.1.1.1 or domain.com
