pipeline {
  agent any
  parameters {
    string(name: 'Version', defaultValue: '1.0.0', description: 'Version Number')
  stages {
    stage('stage-1') {
      parallel {
        stage('stage-1') {
          steps {
            echo 'lets get sttarted'
            echo 'did you here me'
          }
        }

        stage('stage-1a') {
          steps {
            echo 'i heard you'
          }
        }

        stage('stage-1b') {
          steps {
            echo 'then lets go'
          }
        }

      }
    }

    stage('stage-2') {
      steps {
        sh '''#!/bin/bash
echo "we starting ok!"
sleep 10
echo "started aight"'''
      }
    }

    stage('stage-3') {
      steps {
        echo 'one more time'
        sh 'chmod 777 ./start.sh'
        sh './start.sh'
      }
    }

    stage('stage-4') {
      steps {
        echo "${params.Version} to be deployed"
        echo 'we are done'
      }
    }

  }
}
