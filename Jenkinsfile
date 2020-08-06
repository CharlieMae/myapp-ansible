pipeline {
    agent any

     stages {
        stage('GET SOURCE CODE') {
            steps {
                // Get some code from a GitHub repository
                git 'https://github.com/CharlieMae/myapp-ansible.git'
            }

        }
        stage('EXECUTE ANSIBLE PLAYBOOK') {
            steps {
                // Get some code from a GitHub repository
                ansiblePlaybook become: true, credentialsId: 'ubuntu_private_key', disableHostKeyChecking: true, installation: 'ansible', inventory: 'dev.inv', playbook: 'apache.yml'            
            }
        }
    }
}
