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

       stage('Test') {
    steps {
        echo 'Running tests...'

        sh '''
        python3 - <<EOF
import calculator

# Assertions (this is the key part)
assert calculator.add(2,3) == 5, "Add function failed"
assert calculator.subtract(5,2) == 3, 
assert calculator.multiply(3,4) == 12, 
assert calculator.divide(10,2) == 5, 
print("All tests passed")
EOF
        '''
    }
}

        stage('Deploy') {
            steps {
                echo 'Deploy stage (dummy for now)'
            }
        }
    }
}
