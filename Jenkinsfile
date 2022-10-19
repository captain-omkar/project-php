node {
  stage('SCM') {
    checkout scm
  }
  stage('SonarQube bbAnalysis') {
    def scannerHome = tool 'sonar';
    withSonarQubeEnv() {
      sh "${scannerHome}/bin/sonar-scanner"
    }
  }
}
