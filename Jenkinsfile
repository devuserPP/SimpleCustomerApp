pipeline {
    agent any
    stages {
        stage('SonarQube') {
            steps {
                    dir("./SimpleCustomerApp/") {
                    sh 'sonar-scanner'
                    }
            }
        
        
        }
    }
}
