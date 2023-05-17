// pipeline {
//   agent any
//   stages {
//     stage('build') {
//       steps {
//        echo 'build'
//       }
//     }
//     stage('test') {
//       steps {
//         echo 'test'
//       }
//     }
//   }
// }

pipeline{
    agent any
    environment {
        VAR = "${params.VAR}"
    }
    stages {
        stage("Display param") {
            steps {
                script {
                    
                      Echo '{VAR}'
                    
                  
                }
            }
        }
    }
}