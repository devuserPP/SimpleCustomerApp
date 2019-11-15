pipeline {
    agent any
    stages {
        stage('SonarQube') {
            environment {
            scannerHome = tool 'SonarQube'
            }
            
            steps {
                    dir("./SimpleCustomerApp/") {
                        withSonarQubeEnv('SonarQube') {                    
                        sh "${scannerHome}/bin/sonar-scanner"
                        }
                    }
            }
        
        
        }
    }
}
