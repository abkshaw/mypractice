pipeline {
    agent any
    parameters {
        choice(name: 'SELECTED_ENVIRONMENT', choices: ['DEV', 'INTTEST', 'INTEGRATION', 'PREPROD'], description: 'The environment to run tests on.')
        booleanParam(defaultValue: false, description: 'Whether or not to test a release', name: 'CREATE_RELEASE')
    }
    stages {
        stage('Example') {
            steps {
                echo "${params.SELECTED_ENVIRONMENT}"
                script { currentBuild.description = "${params.SELECTED_ENVIRONMENT}" }
            }
        }
    }
}
