pipeline {
    agent any

    parameters {
        string(name: 'BUILD_TRIGGER', defaultValue: 'Anonymous', description: 'Name of the person who triggered this build')
        string(name: 'BRANCH_NAME', defaultValue: 'main', description: 'Branch to build from')
        string(name: 'SOURCE_FILE', defaultValue: 'Main.java', description: 'Path to the Java source file')
    }

    stages {
        stage('Compile') {
            steps {
                echo "Compiling ${params.SOURCE_FILE} by ${params.BUILD_TRIGGER}"
                sh "javac ${params.SOURCE_FILE}"
            }
        }
        stage('Run') {
            steps {
                script {
                    def className = params.SOURCE_FILE.replace('.java', '')
                    echo "Running ${className}"
                    sh "java ${className}"
                }
            }
        }
    }
}
