pipeline {
    agent any 
    stages {
        stage('Cloning Git') {
            steps {
                sh '''
                    #!/bin/bash
                    git clone https://github.com/sravan-github/toolkit.git
                    pwd
                    cd toolkit
                    pwd
                    ls -ltr
                    ansible --version
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
