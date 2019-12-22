node('Slave1'){
  def grdleHome = tool 'gradle4'
  try{
    stage('checkout'){
      checkout scm
      echo 'checkout'
    }
    stage('build') {
      sh "${grdleHome}/bin/gradle build"
      echo 'build finished'
    }
  }catch(ex) {
    echo "Error occured"
  }
  stage('post') {
    if (currentBuild.result == null || currentBuild.result == 'SUCCESS') {
      addBadge(icon: green.gif, text: 'Build succeeded')
    }else {
      addBadge(icon: red.gif, text: 'Build failed')
    }
  }
}
