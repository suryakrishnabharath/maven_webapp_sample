pipeline
{
    agent any
    triggers
    {
        pollSCM('* * * * *')
    }
    stages
    {
        stage('Git-Checkout')
        {
            steps
            {
                echo "Git Checkout"
                git 'https://github.com/suryakrishnabharath/maven_webapp_sample.git'
            }
        }
        stage('Maven-Validate')
        {
            steps
            {
                echo "maven Validate"
                bat 'mvn validate'
            }
        }
        stage('Maven-Compile')
        {
            steps
            {
                echo "maven Compile"
                bat 'mvn compile'
            }
        }
        stage('Maven-test')
        {
            steps
            {
                echo "maven Test"
                bat 'mvn test'
            }
        }
        stage('Maven-Package')
        {
            steps
            {
                echo "maven Package"
                bat 'mvn package'
            }
        }
        stage('Maven-install')
        {
            steps
            {
                echo "maven Install"
                bat 'mvn install'
            }
        }
    }
}
