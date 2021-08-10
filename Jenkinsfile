pileline{
    agent any
    environment{
        //
    }
    tools{
        //
    }
    stages{
        stage('Git Checkout'){
            steps{
                git branch: 'main', url: 'https://github.com/saida-d/ansible-jenkins.git'
                echo "Checkout - Done"
            }
        }
        stage('Execute Ansible'){
            steps{
                ansiblePlaybook credentialsId: 'ansible2-target-private-key', disableHostKeyChecking: true, installation: 'ansible2', inventory: 'hosts.inv', playbook: 'playbook.yml'
                echo "Ansible - Executed"
            }
        }
    }
}
