pipeline{
    agent{ label 'node3'}
    stages{
        stage('vcs'){
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
        
    }

}