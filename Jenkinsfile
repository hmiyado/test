pipeline {
    agent { docker { image 'ruby' } }
    stages {
        stage('build') {
            steps {
                sh 'cd test'
                sh 'jekyll build'
            }
        }
        stage('deploy') {
            steps {
                sh 'jekyll serve --detach'
            }
        }
    }
}
