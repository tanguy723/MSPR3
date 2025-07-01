
Jenkinsfile (Declarative Pipeline)

/* Requires the Docker Pipeline plugin */
pipeline {
    agent any
     stage('Deploy') {
                steps {
                    retry(3) {
                        sh './flakey-deploy.sh'
                    }

                    timeout(time: 3, unit: 'MINUTES') {
                        sh './health-check.sh'
                    }
                }
            }
    }
}

