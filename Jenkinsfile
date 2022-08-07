pipeline{
    agent any
    environment{
        name = "obikhan"
    }
    parameters{
        string(name: 'person', defaultValue: 'obi khan', description: "who  are you?")
    }
    
    stages{
        stage('dev')
        {
            steps{
                echo 'obaid Ullah tabish'
            }
        }
        stage('code_download')
        {
            steps{
                git 'https://github.com/Tabish-0007/samples.git'
            }
        }
        stage('cmdrun')
        {
            steps{
                bat '''
                cd 
                cd /
                cd kubectl
                '''
            }
        }
        stage('Envirment & parameters')
        {
            steps{
                bat 'echo "$(BUILD_ID)"'
                bat 'echo "$(person)"'
            }
        }
    }
    post{
        always{
            echo "i will always run"
        }
        failure{
            echo "fial"
        }
        success{
           echo "success" 
        }
    }
}
