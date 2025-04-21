pipeline{
    agent any{
        stages{
            stage('git clone'){
                steps{
                    sh 'git url'
                }
            }
            stage('build'){
                steps{
                    sh 'mvn clean package'
                }
            }
             stage('test'){
                steps{
                    test cases
                }
            }
        stage('sonar'){
                steps{
                    sh 'sonar :sonar'
                }
            }
        stage('jfrog artfacts'){
            steps{
                    push 'jfrog _url '
                }
            }
        stage('cd triggred'){
                steps{
                    build job: cd dceployed
                }
            }
        }

    }
}