ansiColor('xterm') {
  stage('integration_test') {
    environment {
      RSC_LICENSE = credentials('connectapi-connect-license-key')
    }
    node('docker') {
      checkout scm
      print "Running integration tests"
      echo $RSC_LICENSE
      sh "RSC_LICENSE=$RSC_LICENSE make test"
      print "Finished integration tests"
    }
  }
}
