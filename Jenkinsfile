pipeline {
    agent any
    stages {
        stage('SonarQube') {
            environment {
            SonarQubeScannerHome = tool 'sonar-scanner'
            // in the Global Tool Configuration in Jenkins 
            }
            
            steps {
                    dir("./SimpleCustomerApp/") {
                        withSonarQubeEnv('SonarQube-Server') {                    
                   //     sh "${scannerHome}/bin/sonar-scanner"
                        sh "${SonarQubeScannerHome}/bin/sonar-scanner -Dsonar.host.url=http://my-sonar:9000/sonar -Dproject.settings='sonar-project.properties' -Dsonar.projectBaseDir=."
                        }
                    }
            }
        
        
        }
    }
}
    
