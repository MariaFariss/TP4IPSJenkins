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

// pipeline{
//     agent any
//     environment {
//         VAR = "${params.VAR}"
//     }
//     stages {
//         stage("Display param") {
//             steps {
//                 script {
                    
//                       echo " test   ${VAR}"
                    
                  
//                 }
//             }
//         }
//     }
// }


pipeline {
  agent any
  stages {
    stage('build') {
      steps {
        // echo 'upgrading pip3'
        // sh 'pip3 install --upgrade pip'
        echo 'build'
        bat 'pip3 install -r requirements.txt'
      }
    }
    stage('test') {

      steps {
        echo 'test'
        bat 'python3 -m xmlrunner -o test-reports'
      }
      post {
        always {
          junit 'test-reports/*.xml'
        }
      }
    }
  }
}