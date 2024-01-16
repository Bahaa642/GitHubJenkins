pipeline {
  agent any
  stages {
    stage('Ansible') {
      parallel {
        stage('Ansible') {
          steps {
            ansiblePlaybook(become: true, playbook: 'playbook1', becomeUser: 'bahaa', checkMode: true, colorized: true, disableHostKeyChecking: true, dynamicInventory: true, credentialsId: 'all')
          }
        }

        stage('github') {
          steps {
            git(url: 'https://github.com/Bahaa642/GitHubJenkins.git', branch: 'main')
          }
        }

      }
    }

  }
}