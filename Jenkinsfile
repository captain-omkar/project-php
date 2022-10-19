node {
  stage('SCM') {
    checkout scm
  }
  stage('SonarQdsdube bbAnalysis') {
    def scannerHome = tool 'sonar';
    withSonarQubeEnv() {
      sh "${scannerHome}/bin/sonar-scanner"
    }
  }
}
