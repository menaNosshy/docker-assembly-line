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
  // This step should not normally be used in your script. Consult the inline help for details.
  withDockerContainer('Maven') {
    stages {
        stage('maven') {
          steps {
            sh "mvn -version"
            sh "java -version"
          }
        }
      }
  }
}
