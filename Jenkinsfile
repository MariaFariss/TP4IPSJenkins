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
                    if(VAR)
                    {
                      Echo “my value is true”
                    }
                    else if(VAR)
                    {
                         Echo “my value is false”

                    }
                  
                }
            }
        }
    }
}