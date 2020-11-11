pipeline {
    agent any
    environment {
        DB_ENGINE = 'sqllite'
    }
    stages {
        stage ('Compile Stage') {

            steps 
                {
                    echo "DB ENGINE is '$DB_ENGINE'"
                    sh 'mvn clean compile'
                }
            
        }
        stage ('Testing Stage') {

            steps 
                {
                    sh 'mvn test'
                }
        }
    }
}
