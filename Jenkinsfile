pipeline {
      agent any
      stages {
            stage('Init') {
                  steps {
                        echo 'Hi, this is Nick from Github'
                        echo 'A new line goes right here.'
                        echo 'We are Starting the Testing'
                  }
            }
            stage('Pre-Build') {
                  steps {
                        echo 'This is the Pre-build step.'
                  }
            }
            stage('Build') {
                  steps {
                        echo 'Building Sample Maven Project'
                  }
            }
            stage('Artifact Generation') {
                  steps{
                        sh 'echo "We are generating artifacts for ${BUILD_NUMBER}" > output.txt'
                        archiveArtifacts artifacts: 'output.txt', onlyIfSuccessful: true
                  }
            }
            stage('Deploy') {
                  steps {
                        echo "Deploying in Staging Area"
                  }
            }
            stage('Deploy Production') {
                  steps {
                        echo "Deploying in Production Area"
                  }
            }
      }
}
