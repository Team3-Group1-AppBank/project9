pipeline{
  agent {
    label {
    label 'slave1'
    }
  }
  stages{  
    stage('git-clone'){
     steps{
        checkout([$class: 'GitSCM', branches: [[name: '*/main']], extensions: [], userRemoteConfigs: [[credentialsId: 'team3hook', url: 'https://github.com/Team3-Group1-AppBank/project9.git']]])
     }
    }
    stage('parallel1'){
      parallel{
        stage('actions1'){
          steps{
            sh 'pwd'
          }
        }
        stage('actions2'){
          steps{
            sh 'lscpu'
          }
        }
      }
    }
    stage('parallel2'){
      parallel{
        stage('actions3'){
          steps{
            sh 'pwd'
          }
        }
        stage('actions4'){
          steps{
            sh 'lscpu'
          }
        }
      }
    }
     stage('parallel3'){
      parallel{
        stage('actions5'){
          steps{
            sh 'pwd'
          }
        }
        stage('actions6'){
          steps{
            sh 'lscpu'
          }
        }
      }
    }
     stage('parallel4'){
      parallel{
        stage('actions7'){
          steps{
            sh 'pwd'
          }
        }
        stage('actions8'){
          steps{
            sh 'lscpu'
          }
        }
      }
    }
      stage('codebuild'){
      agent {
        label {
          label 'slave2'
        }
      }
      steps{
        sh 'cat /etc/passwd'
      }
    }
     stage('codebuild'){
      agent {
        label {
          label 'slave3'
                 }
      }
      steps{
        echo 'slave3'
      }
    }
   
  }
}
