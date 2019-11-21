pipeline {
  agent none
  stages {
    stage('Unit Tests') {
      agent {
        label 'apache'
      }
      steps {
        sh 'ant -f test.xml -v'
        junit 'reports/result.xml'
      }
    }
    stage('Build') {
      agent {
        label 'apache'
      }
      steps {
        sh 'ant -f build.xml -v' 
      }
    }
#    stage ('Running on CentOS'){
#      agent {
#        label 'CentOS' 
#      }
#    }
  } 
}
