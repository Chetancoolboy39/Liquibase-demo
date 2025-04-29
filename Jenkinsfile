pipeline {
    agent any

    parameters {
        string(name: 'SCHEMA_NAME', defaultValue: 'default_schema', description: 'Enter schema name')
    }

    stages {
        stage('Liquibase Update') {
            steps {
                script {
                    sh """
                        mvn liquibase:update -DschemaName=${params.SCHEMA_NAME}
                    """
                }
            }
        }
    }
}
