pipeline{
    agent any
    parameters {
        string(name: 'Person', defaultValue: 'Bek', description: 'Who run pipe?')
        text(name: 'TEXT', defaultValue: 'Bek', description: 'Who run pipe?')
        booleanParam(name: 'TOOGLE', defaultValue: true, description: 'Who run pipe?')
        choice(name: 'CHOICE', choices: ['dev', 'prod'], description: 'Choose env')
        password(name: 'PASS', defaultValue: 'Secret', description: 'What is passwd')
    }

    stages {
        stage('Init and Plan') {
            steps {
                echo "Hello ${params.Person}"
            }
        }


        

    }
}