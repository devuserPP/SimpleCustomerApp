pipeline {
    agent any
    stages {
        stage('SonarQube') {
            steps {
                    dir("./SimpleCustomerApp/") {
                    sh 'sonar-scanner'
                    }
            }
        
        post { 
                always { 
                    dir("./SimpleCustomerApp//target/surefire-reports/") {
                    archiveArtifacts artifacts: '*.*', fingerprint: true
                    }
                }
            }   
        }
    }
}
