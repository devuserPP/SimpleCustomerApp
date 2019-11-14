pipeline {
    agent any
    stages {
        stage('SonarQube') {
            environment {
            scannerHome = tool 'SonarQube'
            }
            
            steps {
                    dir("./SimpleCustomerApp/") {
                    sh 'sonar-scanner'
                    sh "${scannerHome}/bin/sonar-scanner"
                    }
            }
        
        
        }
    }
}
