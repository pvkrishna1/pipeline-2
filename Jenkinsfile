pipeline {
    agent any

    stages {
        stage ('Compile Stage') {

            steps {
                withMaven(maven : 'maven3.5.0') {
                    sh "mvn clean compile"
                }
            }
        }

        stage ('Testing Stage') {

            steps {
                withMaven(maven : 'maven3.5.0') {
                    sh "mvn test"
                }
            }
        }


        stage ('install Stage') {
            steps {
                withMaven(maven : 'maven3.5.0') {
                    sh "mvn install"
                }
            }
        }
    }
}
