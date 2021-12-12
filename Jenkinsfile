/*pipeline {
    agent { label 'DEV' }
    options {
        timestamps()
    }    
    stages {
        stage('build') {
            steps {
                sh 'echo "build phase..........."'
            }
        }
        stage('test') {
            steps {
                sh 'echo "test phase............"'
            }
        }
        stage('release') {
            steps {
                sh 'echo "release phase............."'
            }
        }
    }


}*/
pipeline {
    agent { label 'DEV'}
    options { timestamps() }

    stages {
        stage('Build Docker Image') {
            steps {
                sh 'docker build -t alamwasim/myweb-nginx:1.0.0 .'
            }
        }

        stage('Deploy to Dev Environment') {
            // def dockerRun = 'docker run -d -p 8000:80 --name myweb alamwasim/myweb-nginx:1.0.0'
            steps {
                sh 'docker run -d -p 8000:80 --name myweb alamwasim/myweb-nginx:1.0.0'
            }
        }
    }
}

