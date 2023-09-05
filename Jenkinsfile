pipeline {
  agent any
  // tools {
  //   // a bit ugly because there is no `@Symbol` annotation for the DockerTool
  //   // see the discussion about this in PR 77 and PR 52: 
  //   // https://github.com/jenkinsci/docker-commons-plugin/pull/77#discussion_r280910822
  //   // https://github.com/jenkinsci/docker-commons-plugin/pull/52
  //   'org.jenkinsci.plugins.docker.commons.tools.DockerTool' '18.09'
  // }
  environment {
    DOCKER_CERT_PATH = credentials('id-for-a-docker-cred')
  }
  stages {
    stage('foo') {
      steps {
        sh "docker version" // DOCKER_CERT_PATH is automatically picked up by the Docker client
      }
    }
  }
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
