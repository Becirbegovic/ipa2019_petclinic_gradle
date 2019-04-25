pipeline {
  agent none
  stages {
    stage('verify maven:3.6.0-jdk-8') {
      agent {
        docker {
          image 'maven:3.6.0-jdk-8'
        }
      }
      steps {
          sh 'mvn -v'
      }
    }
      stage('Load Groovy Script') {
          steps {
              echo "Example.groovy"

              script {
                  echo "Hallo Scrpit"
                //def example = load "Example.groovy"
             }
          }
        }

    stage('verify maven:3.6.0-jdk-11') {
      agent {
        docker {
          image 'maven:3.6.0-jdk-11'
        }
      }
      steps {
          sh 'mvn -v'
      }
    }
        stage('verify gradle:5.3.1-jdk8') {
      agent {
        docker {
          image 'gradle:5.3.1-jdk8'
        }
      }
      steps {
          sh 'gradle -v'
      }
    }
    stage('verify gradle:5.3.1-jdk11') {
      agent {
        docker {
          image 'gradle:5.3.1-jdk11'
        }
      }
      steps {
          sh 'gradle -v'
      }
    }
  }
}
