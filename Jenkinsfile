node('Slave1'){
  def grdleHome = tool 'gradle4'
  stage('checkout'){
    checkout scm
    echo 'checkout'
  }
  stage('build') {
    sh "${grdleHome}/bin/gradle build"
    echo 'build finished'
  }
  stage('post') {
   
  }
}
