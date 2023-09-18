pipeline{
  agent any
  tools {
    gradle "Gradle 8.3"
  }
  environment{
    GIT_REPO_URL = "https://github.com/WanguiR/java-todo.git"
  }
  stages{
    stage ('clone repository'){
      steps{
        //clone the repository using the git method
        URL: GIT_REPO_URL
      }
    stage('Build Project'){
      sh 'gradle build'
    }
    stage('Run tests'){
      sh 'gradle test'
    }
    }
  }
}
