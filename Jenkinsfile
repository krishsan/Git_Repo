pipeline { 
    agent any 
    options {
        skipStagesAfterUnstable()
    }
    stages {
        stage('Build') { 
            steps { 
                sh 'mkdir kris' 
            }
        }
        stage('Test'){
            steps {
                sh 'cd kris'
                sh 'echo reports/**/*.xml > test.text' 
            }
        }
        stage('Deploy') {
            steps {
                sh 'cat test.text'
            }
        }
    }
}
