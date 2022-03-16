pipeline {
    agent any

    stages 
    {
        stage('Build') 
        {
            steps 
            {
                echo 'Build App'
            }
        }
        
        stage('Test') 
        {
            steps 
            {
                echo 'Test App'
            }
        }
        stage('Deploy') 
        {
            steps 
            {
                echo 'Deploy App'
            }
        }
    }
    post 
    {
        always 
        {
            emailext body: "${currentBuild.currentResult}" , subject: "pipeline status is ${currentBuild.currentResult}", to: 'klakshmansai@stratapps.com'
        }
     }   
}
