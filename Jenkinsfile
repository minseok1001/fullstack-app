pipeline{
    agent any

    environment {
        dockerHubRegistry = 'minseok1001'
        dockerHubRegistryCredential = 'docker-hub'
        githubCredential = 'minseok1001'
    }

    stages {
        stage('check out application git branch'){
            steps {
                checkout scm
            }
            post {
                failure {
                    echo 'repository checkout failure'
                }
                success {
                    echo 'repository checkout success'
                }
            }
        }

        stage('docker image build'){
            steps{
                sh "docker build -t ${dockerHubRegistry}/react:${currentBuild.number} ./frontend"
                sh "docker build -t ${dockerHubRegistry}/react:latest ./frontend"

                sh "docker build -t ${dockerHubRegistry}/nodejs:${currentBuild.number} ./backend"
                sh "docker build -t ${dockerHubRegistry}/nodejs:latest ./backend"

                sh "docker build -t ${dockerHubRegistry}/db:${currentBuild.number} ./mysql"
                sh "docker build -t ${dockerHubRegistry}/db:latest ./mysql"
            }
            post {
                    failure {
                      echo 'Docker image build failure !'
                    }
                    success {
                      echo 'Docker image build success !'
                    }
            }
        }

        stage('Docker Image Push') {
            steps {
                withDockerRegistry([ credentialsId: dockerHubRegistryCredential, url: "" ]) {
                    sh "docker push ${dockerHubRegistry}/react:${currentBuild.number}"
                    sh "docker push ${dockerHubRegistry}/react:latest"

                    sh "docker push ${dockerHubRegistry}/nodejs:${currentBuild.number}"
                    sh "docker push ${dockerHubRegistry}/nodejs:latest"

pipeline{
    agent any

    environment {
        dockerHubRegistry = 'minseok1001'
        dockerHubRegistryCredential = 'docker-hub'
        githubCredential = 'github_cred'
    }

    stages {
        stage('check out application git branch'){
            steps {
                checkout scm
            }
            post {
                failure {
                    echo 'repository checkout failure'
                }
                success {
                    echo 'repository checkout success'
                }
            }
        }

        stage('docker image build'){
            steps{
                sh "docker build -t ${dockerHubRegistry}/react:${currentBuild.number} ./frontend"
                sh "docker build -t ${dockerHubRegistry}/react:latest ./frontend"

                sh "docker build -t ${dockerHubRegistry}/nodejs:${currentBuild.number} ./backend"
                sh "docker build -t ${dockerHubRegistry}/nodejs:latest ./backend"

                sh "docker build -t ${dockerHubRegistry}/db:${currentBuild.number} ./mysql"
                sh "docker build -t ${dockerHubRegistry}/db:latest ./mysql"
            }
            post {
                    failure {
                      echo 'Docker image build failure !'
                    }
                    success {
                      echo 'Docker image build success !'
                    }
            }
        }

        stage('Docker Image Push') {
            steps {
                withDockerRegistry([ credentialsId: dockerHubRegistryCredential, url: "" ]) {
                    sh "docker push ${dockerHubRegistry}/react:${currentBuild.number}"
                    sh "docker push ${dockerHubRegistry}/react:latest"

                    sh "docker push ${dockerHubRegistry}/nodejs:${currentBuild.number}"
                    sh "docker push ${dockerHubRegistry}/nodejs:latest"

                    sh "docker push ${dockerHubRegistry}/db:${currentBuild.number}"
                    sh "docker push ${dockerHubRegistry}/db:latest"

                    sleep 10 /* Wait uploading */
                }
            }
            post {
                    failure {
                      echo 'Docker Image Push failure !'
                      sh "docker rmi ${dockerHubRegistry}/react:${currentBuild.number}"
                      sh "docker rmi ${dockerHubRegistry}/react:latest"

pipeline{
pipeline{
    agent any

    environment {
        dockerHubRegistry = 'minseok1001'
        dockerHubRegistryCredential = 'docker-hub'
        githubCredential = 'github_cred'
    }

    stages {
        stage('check out application git branch'){
            steps {
                checkout scm
            }
            post {
                failure {
                    echo 'repository checkout failure'
                }
                success {
                    echo 'repository checkout success'
                }
            }
        }

        stage('docker image build'){
            steps{
                sh "docker build -t ${dockerHubRegistry}/react:${currentBuild.number} ./frontend"
                sh "docker build -t ${dockerHubRegistry}/react:latest ./frontend"

                sh "docker build -t ${dockerHubRegistry}/nodejs:${currentBuild.number} ./backend"
                sh "docker build -t ${dockerHubRegistry}/nodejs:latest ./backend"

                sh "docker build -t ${dockerHubRegistry}/db:${currentBuild.number} ./mysql"
                sh "docker build -t ${dockerHubRegistry}/db:latest ./mysql"
            }
            post {
                    failure {
                      echo 'Docker image build failure !'
                    }
                    success {
                      echo 'Docker image build success !'
                    }
            }
        }

        stage('Docker Image Push') {
            steps {
                withDockerRegistry([ credentialsId: dockerHubRegistryCredential, url: "" ]) {
                    sh "docker push ${dockerHubRegistry}/react:${currentBuild.number}"
                    sh "docker push ${dockerHubRegistry}/react:latest"

                    sh "docker push ${dockerHubRegistry}/nodejs:${currentBuild.number}"
                    sh "docker push ${dockerHubRegistry}/nodejs:latest"

                    sh "docker push ${dockerHubRegistry}/db:${currentBuild.number}"
                    sh "docker push ${dockerHubRegistry}/db:latest"
"Jenkinsfile" 122L, 4892B
