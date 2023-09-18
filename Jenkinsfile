pipeline{
  agent any
  tools {
    gradle "Gradle 8.3"
  }
  environment{
    GIT_REPO_URL = "https://github.com/WanguiR/java-todo.git"
    GIT_CREDENTIALS_ID="wanguiR"
  }
  stages{
    stage ('clone repository'){
      steps{
        //clone the repository using git method
        gitcredentialsID: GIT_CREDENTIALS_ID,url:GIT_REPO_URL
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
