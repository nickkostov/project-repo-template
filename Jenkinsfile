pipeline {
    agent any

    stages {
        stage ('Compile Stage') {

            steps {
				// could be a build 
                    sh 'echo "Hello There"'
					sh 'pwd'
            }
        }

        stage ('Testing Stage') {
				// could be a tests
            steps {
                    sh 'echo "Hello There Second stage'
					sh 'ls -lah'
                }
            }
        }

				// could be a release
        stage ('Deployment Stage') {
            steps {
                    sh 'echo "I am here"'

            }
        }
}
