pipeline {
    agent any

    stages {
        stage('Clone') {
            steps {
               sh '''
               echo "Code pulled from GitHub"
               '''
            }
        }
        stage('Build') {
            steps {
               sh '''
               echo "Building Project"
               echo "Creating build directory"
               mkdir -p build
               '''
            }
        }
         stage('Write') {
            steps {
               sh '''
               echo "Writing inside build directory"
               echo "Creating file"
               touch build/output.txt
               echo "Build Completed Succesfully" > build/output.txt
               echo "Build number: $BUILD_NUMBER" > build/output.txt
               echo "Writing inside build directory completed"
               '''
            }
        }
    }

    post{
        success{
            archiveArtifacts artifacts: 'build/**'
        }
    }
}
