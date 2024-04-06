pipeline {
    agent { label 'jenkins-abhi1'}

    stages {
        stage ('Compile Stage') {

            steps {
                withMaven(maven : 'maven-3.9.6') {
                    sh 'mvn clean compile'
                }
            }
        }

        stage ('Testing Stage') {

            steps {
                withMaven(maven : 'maven-3.9.0') {
                    sh 'mvn test'
                }
            }
        }


        stage ('Deployment Stage') {
            steps {
                withMaven(maven : 'maven-3.8.6') {
                    sh 'mvn deploy'
                }
            }
        }
    }
}
