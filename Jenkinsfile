pipeline {
    agent any
    tools{
        maven "Maven_3_5_2"
    }
    stages{
        stage('CompileandRunSonarAnalysis'){
            steps{
               sh 'mvn clean verify sonar:sonar -Dsonar.projectkey=prokectkey -Dsonar.organization=organizationkey -Dsonar.host.url=https://sonarcloud.io -Dsonar.login=sonarToken'
            }
            }
        }
    }
}