pipeline {
    agent any

    stages
    {
        stage('pull the image') 
        {
            steps 
            {
                bat "docker pull ashutosh753/newprojectofseleniumjar"
            }
        }

        stage('Start the grid') 
        {
            steps 
            {
                bat "docker-compose up -d selenium-hub chrome firefox"
            }
        }

        stage('Execute Cucumber Test cases') 
        {
            steps 
            {
                bat "docker-compose up seleniumproject"
            }
        }
    }
    post
    {
        always
        {
           bat "docker-compose down"
        }

    }
}
