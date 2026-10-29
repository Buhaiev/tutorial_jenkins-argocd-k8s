pipeline {
  agent { label 'Jenkins-Agent' }

  tools {
    jdk   'Java17'   // use the exact names you gave in Manage Jenkins -> Tools
    maven 'Maven3'
  }

  stages {
    stage('Build') {
      steps {
        dir('CICD_java_app') {
          sh 'mvn clean package -DskipTests'
        }
      }
    }
    stage('Unit test') {
      steps {
        dir('CICD_java_app') {
          sh 'mvn test'
        }
      }
    }
  }
}
