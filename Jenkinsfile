pipeline {
  agent any
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
sleep 60
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
        echo 'we are done'
      }
    }

  }
}