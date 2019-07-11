node {

            stage('Cleaning the WorkSpace')
            {
                deleteDir()
            }

            stage('Checkout the code from GitHub')
            {
                git url: 'https://github.com/anand204/Education.git'
            }

            stage('remove the old code from job')
            {
                sh 'sudo rm -rf /var/www/html/*'
            }

            stage('Deploying the latest code')
            {
                sh 'sudo cp -pr /var/lib/jenkins/workspace/Scripted_Pipline_job/* /var/www/html/'
            }
            stage('Restart the Apache')
            {
                sh 'sudo service httpd restart'
            }
        }
