pipeline {
    agent any

    stages {
        stage('Clone Repository') {
            steps {
                git branch: 'master', url: 'https://github.com/mithun02/apachewebsite-clone'
            }
        }

        stage('Build') {
            steps {
                echo 'Building the project...'
                // Add your build commands here if any
            }
        }

        stage('Deploy to Apache') {
            steps {
                echo 'Deploying to Apache server...'
                sh '''
                    # Example deployment commands
                    sudo cp -r * /var/www/html/
                    sudo systemctl restart apache2
                '''
            }
        }
    }
}
