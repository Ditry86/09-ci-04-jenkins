pipeline {
    agent any
    stages {
        stage('Prepare') {
            steps {
                sh 'rm -rf ansible_study_5'
                sh 'git clone https://github.com/Ditry86/ansible_study_5.git'
                sh 'pip3 install --force-reinstall "urllib3<1.27" "chardet<5.0"'
            }
        }
        stage('Test') {
            steps {
                sh 'cd ansible_study_5/playbook/roles/vector-role && molecule -vvv test'
            }
        }
    }
}