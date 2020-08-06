pipeline {
    agent any

     stages {
        stage('GET SOURCE CODE') {
            steps {
                // Get some code from a GitHub repository
                git 'https://github.com/ravishsubramanya/myapp-ansible.git'
            }

        }
        stage('EXECUTE ANSIBLE PLAYBOOK') {
            steps {
                // Get some code from a GitHub repository
                ansiblePlaybook become: true, credentialsId: 'private-key', disableHostKeyChecking: true, installation: 'ansible', inventory: 'dev.inv', playbook: 'apache.yml'            }
        }
    }
}
