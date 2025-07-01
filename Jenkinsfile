
//Jenkinsfile (Declarative Pipeline)

/* Requires the Docker Pipeline plugin */
pipeline {
    agent {
        docker { image 'node:22.17.0-alpine3.22' }
    }
    stages {
        stage('Test') {
            steps {
                bat 'node --eval "console.log(process.arch,process.platform)"'
            }
        }
    }
}
