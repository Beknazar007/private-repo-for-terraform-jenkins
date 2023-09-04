@Library('mySharedLibrary') _

terraform([
                        awsCredentialId: params.AWS_SECRET_ACCESS_KEY, // Customize as needed
                        backendConfig: [
                            s3_bucket_name: params.TERRAFORM_BACKEND_S3_BUCKET,
                            key_path: params.TERRAFORM_BACKEND_KEY_PATH,
                            aws_region: 'us-east-1'
                        ],
                        envStage: params.ENVIRONMENT
])
// pipeline {
//     agent any
//         parameters {
//             choice(
//                 name: 'ENVIRONMENT',
//                 choices: ['dev', 'prod'],
//                 description: 'Select the environment'
//             )
//             credentials (
//                 credentialType: 'com.cloudbees.jenkins.plugins.awscredentials.AWSCredentialsImpl', 
//                 defaultValue: '' , 
//                 description: '''Select AWS credentials for you to deploy''',
//                 name: 'AWS_SECRET_ACCESS_KEY', 
//                 required: true
//             )
//             text(
//                 description: 'Terraform Backend S3 Bucket Name',
//                 name: 'TERRAFORM_BACKEND_S3_BUCKET',
//                 defaultValue: ''
//             )
//             text(
//                 description: 'Terraform Backend Path',
//                 name: 'TERRAFORM_BACKEND_KEY_PATH',
//                 defaultValue: ''
//             )
//         }
//     stages {
//         stage('Terraform Deployment') {
//             steps {
//                 script {
//                     def terraformConfig = [
//                         awsCredentialId: params.AWS_SECRET_ACCESS_KEY, // Customize as needed
//                         backendConfig: [
//                             s3_bucket_name: params.TERRAFORM_BACKEND_S3_BUCKET,
//                             key_path: params.TERRAFORM_BACKEND_KEY_PATH,
//                             aws_region: 'us-east-1'
//                         ],
//                         envStage: params.ENVIRONMENT
//                     ]

//                     // Load the terraform.groovy library


//                     // Call the 'call' function from the loaded library
//                     terraform(terraformConfig)
//                 }
//             }
//         }
//     }
// }