pipeline {
    agent any
    stages {
        stage('Run Jobs in Parallel') {
            parallel {
                stage('Job A') {
                    steps {
                        build job: 'Python_Job'
                    }
                }
                stage('Job B') {
                    steps {
                        build job: 'Simple_Maven_Project_Pipeline'
                    }
                }
            }
        }
        stage('Run Job C') {
            steps {
                build job: 'Ansible_Job'
            }
        }
    }
}
