env.JAVA_HOME = '/usr/lib/jvm/java-17-openjdk-amd64'

pipeline {
  agent { docker "maven" }

  stages {
    stage('maven') {
      steps {
        sh "mvn -version"
        sh "java -version"
      }
    }
  }
}
