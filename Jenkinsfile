pipeline {
    agent any

    stages {
        stage('git-clone') {
            steps {
                git 'https://github.com/sivaji348/game-of-life.git'
            }
        }
         stage('compile') {
            steps {
               sh 'mvn compile'
            }
        }
        stage('review') {
            steps {
               sh 'mvn pmd:pmd'
            }
        }
        stage('test') {
               steps {
    // One or more steps need to be included within the steps block.
                 sh 'mvn test'
  }
        }
  stage('coverage') {
            steps {
               sh 'mvn cobertura:cobertura -Dcobertura.report.format=xml'
            }
        }
        stage('package') {
            steps {
               sh 'mvn package'
            }
        }
}
    }


