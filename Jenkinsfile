@Library('MySharedLib') _

terraform([
                        awsCredentialId: params.AWS_SECRET_ACCESS_KEY, // Customize as needed
                        backendConfig: [
                            s3_bucket_name: params.TERRAFORM_BACKEND_S3_BUCKET,
                            key_path: params.TERRAFORM_BACKEND_KEY_PATH,
                            aws_region: 'us-east-1'
                        ],
                        envStage: params.ENVIRONMENT
])
