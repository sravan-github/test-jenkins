pipeline {
    agent {
     docker { image 'ansible' }
    }
    stages {
        stage('Cloning Git') {
            steps {
                sh '''
                    #!/bin/bash
                    #git clone https://github.com/sravan-github/toolkit.git
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
