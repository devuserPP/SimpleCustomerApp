pipeline {
    agent any
    stages {
        stage('SonarQube') {
            environment {
            scannerHome = tool 'sonar-scanner'
            // in the Global Tool Configuration in Jenkins 
            }
            
            steps {
                    dir("./SimpleCustomerApp/") {
                        withSonarQubeEnv('SonarQube-Server') {                    
                   //     sh "${scannerHome}/bin/sonar-scanner"
                        sh "${sonarqubeScannerHome}/bin/sonar-scanner -Dsonar.host.url=http://http://localhost:90/sonar -Dproject.settings='sonar-project.properties' -Dsonar.projectBaseDir=."
                        }
                    }
            }
        
        
        }
    }
}
    
