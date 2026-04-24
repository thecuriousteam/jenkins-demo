pipeline {
    agent any

    stages {
        stage('Clone & Cat') {
            steps {
               sh '''
               echo "Code pulled from GitHub"
               ls
               cat index.html
               '''
               
            }
        }
    }
}
