pipeline {
    
    agent any
    tools {
        maven 'MAVEN 3.6.3'
    }
    stages {
        stage('clone and clean') {
            steps {
                bat "git clone https://github.com/ShashankFuley/springboot-ecommerce.git"
                bat "mvn clean -f springboot-ecommerce"
            }
        }
        stage('Test') {
            steps {
                bat "mvn test -f springboot-ecommerce"
            }
        }
        stage('Deploy') {
            steps {
                bat "mvn package -f springboot-ecommerce"
            }
        }
    }
}
