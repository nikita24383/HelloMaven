pipeline {
  agent any
  tools {
  maven 'MAVEN'
  }
  stages {
    stage ('Build') {
      steps {
        bat 'mvn clean package'
      }
    }
  }
  post{
    always{
      junit(
      allowEmptyResults: true,
      testResults: '*test-report/.xml'
      )
    }
  }
}
