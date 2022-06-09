pipeline{
  agent any
  stages{
    stage('version control'){
      steps{
        git checkout 
      }
    }
    stages('parallel job1'){
      parallel{
        stage('sub-job1'){
          steps{
            sh 'system start Jenkins'
            sh 'lsblk'
          }
        }
      }
    }
  }
}