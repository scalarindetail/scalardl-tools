pipeline {
  agent any
  stages {
    stage('Run Emulator Tests') {
      steps {
        dir(path: './emulator') {
          pwd()
          sh './gradlew assemble'
          sh './gradlew test'
        }

      }
    }
    stage('Notify') {
      steps {
        mail(to: 'siyopao@gmail.com', from: 'jenkins', subject: 'Build finished', body: 'Hi there!')
      }
    }
  }
}