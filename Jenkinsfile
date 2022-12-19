pipeline{
    agent{ label 'node3'}
    triggers {
        pollSCM('* * * * *')
    }
    stages{
        stage('git clone'){
            steps{
                git url: 'https://github.com/peddiraju3122b/devopsworkshop.git',
                branch: 'main'
            }
        }
        stage('image build'){
            steps{
                sh 'docker image build -t peddiraju3122b/devopsworkshop:DEV .'

            }
        }
        stage('push image to registry'){
            steps{
                sh 'docker image push peddiraju3122b/devopsworkshop:DEV'
            }
        }
    }

}