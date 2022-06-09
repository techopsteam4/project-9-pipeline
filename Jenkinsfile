pipeline{
  agent any
  stages{
    stage('version control'){
      steps{
        checkout([$class: 'GitSCM', branches: [[name: '*/main']], extensions: [], userRemoteConfigs: [[credentialsId: 'Github-id', url: 'https://github.com/techopsteam4/project-9-pipeline.git']]])
      }
    }
    stage('parallel job1'){
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
