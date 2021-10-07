pipeline {
    agent any

    stages {
        stage('build') {
            
            agent {
                docker {
                    image 'maven'
                    args ' -u root  -v $PWD:/usr/src/mymaven -w /usr/src/mymaven '
                }
                
            }
            steps {
                
                sh 'mvn clean install '

            }
        }
    }
}
