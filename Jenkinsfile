pipeline {
    agent any;
    stages {

        stage('Checkout') {
            steps {

                checkout([$class: 'GitSCM', branches: [[name: '*/master']], doGenerateSubmoduleConfigurations: false, extensions: [], submoduleCfg: [], userRemoteConfigs: [[credentialsId: '', url: 'https://github.com/szaher/freezer-api']]])
            }
        }
        stage('check') {

            steps {
                parallel(
                        containers: {
                            sh "ls -lh"
                        },
                        images: {
                            sh "pwd"
                        }
                )
            }
        }
        stage('deploy'){
            steps {
                input ('Are you sure you want to deploy ?')
                // if you set wait to true, this will ask the current job to wait till the deploy job is finished!
                # build job: 'deploy-cats-demo-pipeline', wait: false
                sh ' echo "building and deploying" '
                
            }
        }
    }
}
