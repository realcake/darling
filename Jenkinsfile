pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                sh 'git remote set-url origin https://github.com/darlinghq/darling.git'
                sh 'git submodule sync'
                sh 'git submodule update --recursive --init'
                sh 'cmake -E remove_directory build'
                sh 'cmake -Bbuild -H.'
                sh 'cmake --build build'
            }
        }
    }
}
