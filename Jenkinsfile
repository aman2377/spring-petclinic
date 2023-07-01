pipeline {
  agent any
  stages {
    stage('Compile') {
      steps {
        sh './mvnw clean compile'
      }
    }

    stage('Static Analysis') {
      steps {
        sh '''mvn clean verify sonar:sonar \\
  -Dsonar.projectKey=Petclinic \\
  -Dsonar.projectName=\'Petclinic\' \\
  -Dsonar.host.url=http://13.200.3.8:9000 \\
  -Dsonar.token=sqp_34eb66200324d5f986094c7cbbc69f91d9aa3aaf'''
      }
    }

  }
}