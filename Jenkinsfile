pipeline {
    agent any

    stages {

        stage('Checkout') {
            steps {
                echo 'Checking out code...'
                checkout scm
            }
        }

        stage('Build') {
            steps {
                echo 'Building project...'
                sh 'ls -l'
            }
        }

       stage('Test') { steps { echo 'Running tests...' // Run all calculator functions (example) sh ''' python3 - <<EOF from calculator import add, subtract, multiply, divide print("Add:", add(2, 3)) print("Subtract:", subtract(5, 2)) print("Multiply:", multiply(3, 4)) print("Divide:", divide(10, 2)) EOF ''' } }

        stage('Deploy') {
            steps {
                echo 'Deploy stage (dummy for now)'
            }
        }
    }
}
