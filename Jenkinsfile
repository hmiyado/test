pipeline {
    agent { docker { 
        image 'jekyll/jekyll' 
        args '-p 4000:4000'
    } }
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
