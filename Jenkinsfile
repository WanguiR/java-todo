pipeline{
  agent any
  tools {
    gradle "Gradle 8.3"
  }
  stages{
    stage ('clone repository'){
       environment{
        GIT_REPO_URL = "https://github.com/WanguiR/java-todo.git"
      }
      steps{
          //clone the repository using the git method
          url:"GIT_REPO_URL"
      }
    stage('Build Project'){
      steps{
        sh 'gradle build'
      }
    }
    stage('Run tests'){
      steps{
       sh 'gradle test'   
      }
    }
    }
  }
}
