peline {
    agent any
    stages {
        stage('Checkout') {
            steps {
                git 'https://github.com/Bhuvanasachin/Mavendemo.git'
            }
        }
         stage('Build') {
            steps {
              sh 'mvn clean package'
            }
        }
    }
}
