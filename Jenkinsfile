pipeline{
  agent any 
  stages{
    stage('version-control'){
      steps{
        checkout([$class: 'GitSCM', branches: [[name: '*/main']], extensions: [], userRemoteConfigs: [[url: 'https://github.com/techopsteam4/project-9-pipeline.git']]])
      }
    }
    stage('parallel-job1'){
      parallel{
        stage('sub-job1'){
          steps{
            echo 'action1'
          }
        }
        stage('sub-job2'){
          steps{
            echo 'action2'
          }
        }
      }
    }
    stage('code-build'){
      steps{
        sh 'cat /etc/passwd'
      }
    }
  }
}
