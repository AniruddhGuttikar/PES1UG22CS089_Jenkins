pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                sh '''
                echo "Compiling PES1UG2CCS089.cpp"
                g++ PES1UG22CS089.cpp -o PES1UG2CCS089
                '''
            }
        }

        stage('Test') {
            steps {
                sh '''
                echo "Running the compiled program"
                ./PES1UG2CCS089
                '''
            }
        }

        stage('Deploy') {
            steps {
                echo "Deployment step"
            }
        }
    }

    post {
        failure {
            echo "Pipeline failed"
        }
    }
}
