pipeline{
    agent any
    stages{
        stage("get url from git"){
            steps{
                git url : "https://github.com/sibi51/JenkinsTerraform.git", branch : "main"
            }
        }
        stage("terraform init"){
            steps{
                sh "terraform init"
            }
        }
        stage("terraform validate"){
            steps{
                sh "terraform validate"
            }
        }
        stage("terraform plan"){
            steps{
                sh "terraform plan"
            }
        }
        stage("terraform apply"){
            steps{
                sh "terraform apply --auto-approve"
            }
        }
        stage("terraform destroy"){
            steps{
                sh "terraform destroy --auto-approve"
            }
        }
    }
}
