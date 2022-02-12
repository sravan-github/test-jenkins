pipeline {
    agent any 
    stages {
        stage('Cloning Git') {
            steps {
                sh '''
                    #!/bin/bash
                    git clone https://github.com/sravan-github/test-jenkins.git
                    cd test-jenkins
                    pwd
                    ls -ltr
                    ansible --version
                    ansible-playbook shell.yml
                    '''
                }
           }
        }
        post {
        always {
            cleanWs deleteDirs: true
        }
     }
}
