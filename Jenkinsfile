pipeline {
    agent any

    stages {
        stage('Run Command on Jenkins Agent') {
            steps {
                // Use the sh step to run a shell command on the agent
                sh """
                    # Your shell command here
                    echo "Hello, world!"
                    # You can run multiple commands by separating them with newlines
                    ls -l
            }
        }
    }
}




// pipeline {
//     agent any
//     stages {
//         stage('Build Docker Image') {
//             steps {
//                 script {
//                     docker.build('my-docker-image:latest')
//                 }
//             }
//         }
//     }
// }



// pipeline {
//     agent {
//         docker { image 'node:18.17.1-alpine3.18' }
//     }
//     stages {
//         stage('Test') {
//             steps {
//                 sh 'node --version'
//             }
//         }
//     }
// }



// pipeline {
//   agent any
//   tools {
//     // a bit ugly because there is no `@Symbol` annotation for the DockerTool
//     // see the discussion about this in PR 77 and PR 52: 
//     // https://github.com/jenkinsci/docker-commons-plugin/pull/77#discussion_r280910822
//     // https://github.com/jenkinsci/docker-commons-plugin/pull/52
//     'org.jenkinsci.plugins.docker.commons.tools.DockerTool' '18.09'
//   }
//   environment {
//     DOCKER_CERT_PATH = credentials('id-for-a-docker-cred')
//   }
//   stages {
//     stage('foo') {
//       steps {
//         sh "docker version" // DOCKER_CERT_PATH is automatically picked up by the Docker client
//       }
//     }
//   }
// }




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
