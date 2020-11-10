pipeline {
    agent any
    tools {
        maven 'Maven_3.0.5' 
    }

    stages {
        stage ('Compile Stage') {

            steps 
                {
                    sh 'mvn clean compile'
                }
            
        }

        
    }
}
