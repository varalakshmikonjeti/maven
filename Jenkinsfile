pipeline {
    agent{
        label 's1'
    }

    stages {
        stage('SCM') {
            steps {
                git branch:'main',url: "https://github.com/ramyachetty/maven.git"
                git branch:'feature',url: "https://github.com/varalakshmikonjeti/maven.git"
                
            }
        }
        stage('clean')
        {
        steps{
           sh 'mvn clean'
             }
        }
        stage('compile')
        {
        steps{
            sh 'mvn compile'
             }
        }
        stage('test')
        {
        steps{
           sh 'mvn test'
            }
        }
        stage('package')
        {
        steps{
           sh 'mvn package'
             }
        }
    }
}
