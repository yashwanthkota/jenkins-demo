pipeline{
    agent {label 'worker'}
    options {
        buildDiscarder(logRotator(daysToKeepStr: '7'))
        disableConcurrentBuilds()
        retry(3)
        timeout(time: 1,unit: 'MINUTES')
    }
    parameters{
        string(name: 'BRANCH', defaultValue: 'master', description: 'Enter Branch')
        choice(name: 'OPERATION', choices: ['A', 'B', 'C'])
    }
    stages{
        stage("Unit testing"){
            steps{
                sh "echo Hello to Jenkins file and this stage is unit testing"
            }
        }
        stage("Build"){
            steps{
                sh "echo This stage is Build"
                sh "sleep 10"
            }
        }
    }
}
