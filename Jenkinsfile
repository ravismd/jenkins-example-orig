pipeline {
    agent any
    parameters {
        choice(name: 'VERSION', choices: ['1.2.2', '1.2.3'], description: 'Build version')
        booleanParam(name: 'executeTest', defaultValue: 'true', descriptiom: ' ')
    }
    stages {
        when{
            expression{
                param.executeTest == 'true'
            }
        }
        stage ('Compile Stage') {

            steps 
                {
                    
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
