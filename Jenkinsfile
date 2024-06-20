pipeline {
    agent any
    environment {
        // Using returnStdout
        CC = 'clang'
    }
    stages {
        stage('Build') {
            steps {
                echo 'Building..'
            }
        }
        stage('Example') {
            environment {
                DEBUG_FLAGS = '-g'
            }
            steps {
                echo "Running ${env.BUILD_ID} on ${env.JENKINS_URL}"
            }
        }
        stage('Test') {
            steps {
                echo 'Testing..'
                // script {
                //     def browsers = ['chrome', 'firefox']
                //     for (int i = 0; i < browsers.size(); ++i) {
                //         echo "Testing the ${browsers[i]} browser"
                //     }
                // }
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying....'
            }
        }
    }
}