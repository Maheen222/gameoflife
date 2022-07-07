pipeline {
    agent any

    stages {
        stage('git-clone') {
          git 'https://github.com/sivaji348/game-of-life.git'
          sh 'mvn compile'
            }
        }
    }
