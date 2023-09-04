@Library('mySharedLibrary') _
pipeline {
    agent any

    stages {
        stage('Terraform Deployment') {
            steps {
                script {
                    def terraformConfig = [
                        awsCredentialId: 'your-aws-credential-id', // Customize as needed
                        backendConfig: [
                            s3_bucket_name: 'your-s3-bucket-name',
                            key_path: 'your-dynamodb-table',
                            aws_region: 'us-east-1'
                        ]
                    ]

                    // Load the terraform.groovy library
                    load 'path/to/terraform.groovy'

                    // Call the 'call' function from the loaded library
                    terraform(terraformConfig)
                }
            }
        }
    }
}