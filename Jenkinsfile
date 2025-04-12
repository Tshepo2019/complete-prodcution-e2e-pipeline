pipeline{

    agent{
        label "jenkins-agent"
    }

    tool {
        jdk 'Java17'
        maven 'Maven3'
    }

    stages{
        stage["Cleanup Workspace"]{
            steps{
                cleanWs()
            }
        }

        stage["Chout from SCM"]{
            steps{
                git branch 'main', credentialsId: 'github', url 'https://github.com/Tshepo2019/complete-prodcution-e2e-pipeline'
            }
        }
    }

}