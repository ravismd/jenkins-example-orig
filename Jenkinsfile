pipeline {
    agent any
    parameters {
        choice(name: 'VERSION', choices: ['1.2.2', '1.2.3'], description: 'Build version') 
        booleanParam(name: 'executeTest', defaultValue: 'true', description: ' ')
    }
    stages {
      
        stage ('Compile Stage') {
              when{
            expression{
                params.VERSION == '1.2.7' 
            }
        }

            steps 
                {
                    echo "Inside stage Complile"
                    
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
