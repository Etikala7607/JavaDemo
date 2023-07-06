pipeline {
    agent any

    environment {
        function_name = 'sample-java-app'
    }

    stages {
        stage('Build') {
            steps {
                echo 'Build'
                sh 'mvn clean install'
            }
        }
    stage('SonarQube analysis'){
            agent any
            steps{
                withSonarQubeEnv('Sonar'){
                    sh'mvn sonar:sonar'
                }
            }
        }

        stage('Test') {
            steps {
                echo 'Test'
            }
        }

       
            }
        }
    
