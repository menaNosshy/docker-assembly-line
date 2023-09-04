// pipeline {
//   agent { docker "maven" }

//   stages {
//     stage('maven') {
//       steps {
//         sh "mvn -version"
//         sh "java -version"
//       }
//     }
//   }
// }

pipeline {
  agent { docker "maven" }

  stages {
    // This step should not normally be used in your script. Consult the inline help for details.
    stages {
      withDockerContainer('maven') {
          stage('maven') {
            steps {
              sh "mvn -version"
              sh "java -version"
            }
          }
        }
    }
  }
}
