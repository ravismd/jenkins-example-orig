pipeline {
    agent any
    parameters {
        
        booleanParam(name: 'executeTest', defaultValue: 'true', description: ' ')
    }
    stages {
      
        stage ('Compile Stage') {
              when{
            expression{
                params.executeTest == 'true' 
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
