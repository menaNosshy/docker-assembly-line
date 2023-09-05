stages {
    stage('Test Docker') {
        steps {
            sh "docker --version"
        }
    }
    // Other stages in your pipeline
}




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

// pipeline {
//   agent { docker "maven" }

//   stages {
//     // This step should not normally be used in your script. Consult the inline help for details.
//       stage('maven') {
//         withDockerContainer('maven') {  
//             steps {
//               sh "mvn -version"
//               sh "java -version"
//             }
//           }
//         }
//   }
// }
