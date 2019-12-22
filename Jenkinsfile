node('Slave1'){
  def grdleHome = tool 'gradle4'
  stage('checkout'){
    checkout scm
  }
  stage('build') {
    sh "${grdleHome}/bin/gradle build"
  }
  stage('post') {
   
  }
}
