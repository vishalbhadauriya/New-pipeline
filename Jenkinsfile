node {
  stage('SCM') {
    checkout scm
  }
  stage('SonarQube Analysis') {
    def scannerHome = tool 'sonar-scanner';
    withSonarQubeEnv() {
      sh "${scannerHome}/opt/sonar-scanner/bin/"
    }
  }
}
