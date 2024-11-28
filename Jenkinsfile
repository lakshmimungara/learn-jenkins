// pipeline {
//     agent any
//     stages {
//         stage('Build') {
//             steps {
// 			    sh "echo This is build"
//             }
//         }
//         stage('Test') {
//             steps {
// 			    sh "echo This is test"
//             }
//         }
//         stage('Deploy') {
//             steps {
// 			    sh "echo This is deploy"
//             }
//         }
//     }
// }

// pipeline {
//     agent any
//     stages {
//         stage('Build') {
//             steps {
// 				sh "echo This is build"
//             }
//         }
//         stage('Test') {
//             steps {
// 				sh "echo This is test"
//             }
//         }
//         stage('Deploy') {
//             steps {
// 				sh "echo This is deploy"
//             }
//         }
//     }
// 	post {
// 		always{
// 			echo "This section runs always"
// 		}
// 		success{
// 			echo "This section run when pipeline success"
// 		}
// 		failure{
// 			echo "This section run when pipeline failures"
// 		}
// 	}
// }

// pipeline {
//     agent {
// 		label 'AGENT-1'
// 	}
//     stages {
//         stage('Build') {
//             steps {
// 				sh "echo This is build"
//             }
//         }
//         stage('Test') {
//             steps {
// 				sh "echo This is test"
//             }
//         }
//         stage('Deploy') {
//             steps {
// 				sh "echo This is deploy"
//             }
//         }
//     }
// 	post {
// 		always{
// 			echo "This section runs always"
// 		}
// 		success{
// 			echo "This section run when pipeline success"
// 		}
// 		failure{
// 			echo "This section run when pipeline failures"
// 		}
// 	}
// }

// pipeline {
//     agent {
// 		label 'AGENT-1'
// 	}
//     stages {
//         stage('Build') {
//             steps {
// 				sh "echo This is build"
//             }
//         }
//         stage('Test') {
//             steps {
// 				sh "echo This is test"
//             }
//         }
//         stage('Deploy') {
//             steps {
// 				sh "echo This is deploy"
//             }
//         }
//     }
// 	post {
// 		always{
// 			echo "This section runs always"
// 			deleteDir()
// 		}
// 		success{
// 			echo "This section run when pipeline success"
// 		}
// 		failure{
// 			echo "This section run when pipeline failures"
// 		}
// 	}
// }

// pipeline {
//     agent {
// 		label 'AGENT-1'
// 	}
// 	options{
// 		timeout(time: 10, unit: 'SECONDS')
// 	}
//     stages {
//         stage('Build') {
//             steps {
// 				sh "echo This is build"
// 				sh 'sleep 10' 
//             }
//         }
//         stage('Test') {
//             steps {
// 				sh "echo This is test"
//             }
//         }
//         stage('Deploy') {
//             steps {
// 				sh "echo This is deploy"
//             }
//         }
//     }
// 	post {
// 		always{
// 			echo "This section runs always"
// 			deleteDir()
// 		}
// 		success{
// 			echo "This section run when pipeline success"
// 		}
// 		failure{
// 			echo "This section run when pipeline failures"
// 		}
// 	}
// }

// pipeline {
//     agent {
// 		label 'AGENT-1'
// 	}
// 	options{
// 		timeout(time: 10, unit: 'MINUTES')
// 	}
//     stages {
//         stage('Build') {
//             steps {
// 				sh "echo This is build"
// 				// sh 'sleep 10' 
//             }
//         }
//         stage('Test') {
//             steps {
// 				sh "echo This is test"
//             }
//         }
//         stage('Deploy') {
//             steps {
// 				sh "echo This is deploy"
//             }
//         }
//     }
// 	post {
// 		always{
// 			echo "This section runs always"
// 			deleteDir()
// 		}
// 		success{
// 			echo "This section run when pipeline success"
// 		}
// 		failure{
// 			echo "This section run when pipeline failures"
// 		}
// 	}
// }

// pipeline {
//     agent {
// 		label 'AGENT-1'
// 	}
// 	options{
// 		timeout(time: 10, unit: 'MINUTES')
// 		disableConcurrentBuilds()
// 	}
//     stages {
//         stage('Build') {
//             steps {
// 				sh "echo This is build"
// 				// sh 'sleep 10' 
//             }
//         }
//         stage('Test') {
//             steps {
// 				sh "echo This is test"
//             }
//         }
//         stage('Deploy') {
//             steps {
// 				sh "echo This is deploy"
//             }
//         }
//     }
// 	post {
// 		always{
// 			echo "This section runs always"
// 			deleteDir()
// 		}
// 		success{
// 			echo "This section run when pipeline success"
// 		}
// 		failure{
// 			echo "This section run when pipeline failures"
// 		}
// 	}
// }

pipeline {
    agent {
		label 'AGENT-1'
	}
	options{
		timeout(time: 10, unit: 'MINUTES')
		disableConcurrentBuilds()
		retry(1)
	}
    stages {
        stage('Build') {
            steps {
				sh "echo This is build"
				// sh 'sleep 10' 
            }
        }
        stage('Test') {
            steps {
				sh "echo This is test"
            }
        }
        stage('Deploy') {
            steps {
				sh "echo This is deploy"
				error 'pipeline failed'
            }
        }
    }
	post {
		always{
			echo "This section runs always"
			deleteDir()
		}
		success{
			echo "This section run when pipeline success"
		}
		failure{
			echo "This section run when pipeline failures"
		}
	}
}