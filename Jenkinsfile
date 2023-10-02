pipeline {
    agent any
    parameters {
        choice(name: 'Env', choices: ['Dev', 'Prod'], description: 'Pick Environment')
    }
    stages {
        stage('Clone') {
            steps {
                // git branch: 'main', url: 'https://github.com/Abdelrhmxn/IAC-Terraform.git'
                sh "ls"
            }
        }
        // stage('Terraform Init'){
        //     steps{
        //         sh "terraform init"
        //     }
        // }
        stage('Select Workspace'){
            steps{
                withCredentials([usernamePassword(credentialsId: 'aws', usernameVariable: 'AWS_ACCESS_KEY_ID', passwordVariable: 'AWS_SECRET_ACCESS_KEY')]) {
                    script{
                        if (params.Env == 'Dev') {   
                            sh "echo $AWS_ACCESS_KEY_ID"
                        } else {
                            sh "echo $AWS_ACCESS_KEY_ID"
                        }
                    }
                }

            }
        }
        // stage('Terraform Apply'){
        //     steps{
        //         script{
        //             if (params.Env == 'Dev') {   
        //                 sh "terraform apply --var-file dev.tfvars"
        //             } else {
        //                 sh "terraform apply --var-file prod.tfvars"
        //             }
        //         }
        //     }
        // }

    }
}
