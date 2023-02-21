pipeline{
    agent any
    stages{
        stage("Clean Up"){
            steps{
                deleteDir()
            }
        }
        stage("Clone Repo"){
            steps{
                bat "git clone https://github.com/Marknewcomb/Jenkinsapp.git"
            }
        }
        stage("Build"){
            steps{
                dir("Jenkinsapp"){
                    bat "mvn clean install"
                }
            }
        }
        stage("Test"){
            steps{
                dir("Jenkinsapp"){
                    bat "mvn test"
                }
            }
        }
    }
}