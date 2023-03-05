pipeline {
    agent {
  label 'centos'
}
    stages {
        stage('Download vector role') {
            steps {
                git branch: 'main', url: 'https://github.com/fonru/ansible-vector.git'
            }
        }
        stage('Run molecule test vector role') {
            steps {
                sh 'cd vector-role && molecule test'
            }
        }
    }
}