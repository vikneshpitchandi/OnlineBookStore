pipeline {
  agent any
  tools {
    maven 'maven_3.9.11'  // Must match the name you configured
  }

  stages {
    stage('Build JAR') {
      steps {
        git url: 'https://github.com/your-org/your-repo.git', branch: 'main'
        sh 'mvn clean package'
        archiveArtifacts artifacts: '**/target/*.jar', fingerprint: true
      }
    }
  }
}
