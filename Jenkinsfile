pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                echo 'Running build automation'
                sh './gradlew build --no-daemon'
                archiveArtifacts artifacts: 'dist/trainSchedule.zip'
            }
        }
        stage('AfterBuild'){
            steps{
                input 'Is ready for production?'
                echo 'You are on after build stage please mention what to nbe done'
            }
        }
    }
}
