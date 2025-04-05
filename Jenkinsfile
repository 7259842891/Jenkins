pipleline{
  agent any
  stages{
    stage('one'){
      steps{
        echo 'this is pipeline'
      }
    }
    stage('two'){
      steps{
        input('do you want to procced')
      }
    }
stage('three'){
  when{
    not{
      branch 'master'
    }
  }
  steps {
    echo 'hello'
  }
}
    stage('four') {
      parallel {
        stage('unit test') {
          stepd {
            echo 'running the unit test.'
          }
        }
        stage('integration test') {
          agent {
            docker {
              resuseNode false
              image 'ubuntu'
            }
          }
          steps {
            echo 'running the integration test.'
          }
        }
      }
    }
  }
}

