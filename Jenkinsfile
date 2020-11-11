pipeline {
    agent any
    parameters {
        choice(name: 'VERSION', choices: ['1.2.2', '1.2.3'], description: 'Build version')
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
