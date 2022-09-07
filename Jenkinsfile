pipeline{

  agent any

  stages{  

    stage('git-clone'){

     steps{

        checkout([$class: 'GitSCM', branches: [[name: '*/main']], extensions: [], userRemoteConfigs: [[credentialsId: 'team3hook', url: 'https://github.com/Team3-Group1-AppBank/project9.git']]])

     }

    }

   stage('parallel1'){

      parallel{

        stage('victoria'){

          steps{

            sh 'bash -x /var/lib/jenkins/project9/victoria.sh'

          }

        }

        stage('temitope'){

          steps{

            sh 'bash -x /var/lib/jenkins/project9/temitope.sh'
            echo 'testing'

          }

        }

      }

    }

    stage('parallel2'){

      parallel{

        stage('daniel'){

          steps{

            sh 'bash -x /var/lib/jenkins/project9/daniel.sh'

          }

        }

        stage('joe'){

          steps{

            sh 'bash -x /var/lib/jenkins/project9/joe.sh'

          }

        }

      }

    }

     stage('parallel3'){

      parallel{

        stage('sukhman'){

          steps{

            sh 'bash -x /var/lib/jenkins/project9/sukhman.sh'

          }

        }

        stage('kingsley'){

          steps{

            sh 'bash -x /var/lib/jenkins/project9/kingsley.sh'

          }

        }

      }

    }

     stage('parallel4'){

      parallel{

        stage('gloria'){

          steps{

            sh 'bash -x /var/lib/jenkins/project9/gloria.sh'

          }

        }

        stage('frank'){

          steps{

            sh 'bash -x /var/lib/jenkins/project9/frank.sh'

          }

        }

      }

    }

  }

}
