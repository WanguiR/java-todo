pipeline{
  agent any
  tools {
    gradle "Gradle 8.3"
  }
  stages{
    stage ('clone repository'){
       environment{
        GITHUB_REPO_URL = "https://github.com/WanguiR/java-todo.git"
        GITHUB_ID = "wanguiR"
      }
      steps{
        //clone the repository using the git method
        git ID :GITHUB_ID  , giturl : GITHUB_REPO_URL
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
