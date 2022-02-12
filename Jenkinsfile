pipeline {
    agent any 
    stages {
        stage('Cloning Git') {
            steps {
                sh '''
                    #!/bin/bash
                    git clone https://github.com/sravan-github/toolkit.git
                    cd toolkit
                    pwd
                    ls -ltr
                    ansible --version
                    ansisble-playbook shell.yml
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
