pipeline {
    agent any
    tools{
        maven "Maven_3_5_2"
    }
    stages{
         stage(Build){
         steps{
                withDockerRegistry([credentialsId: "dockerlogin",url;""])
                    script{
                        app = docker.build("hd")
                        }
                    }
                }
        stage(Push) {
            steps {
                script{
                        docker.withRegistry('https://058264359241.dkr.ecr.us-east-1.amazonaws.com','ecr-us-east-1:aws-credentials')
                        app.push("latest")
                            }
                        }
                    }
             }
        }
    

