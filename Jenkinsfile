pipeline {
    agent any

    stages
    {
        stage('Execute Cucumber Test cases') 
        {
            steps 
            {
                bat "docker-compose up"
            }
        }
        
        stage('Close Docker compose After Exceution') 
        {
            steps
            {
                bat "docker-compose down"
            }
        }
    }
}
