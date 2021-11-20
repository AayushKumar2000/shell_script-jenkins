pipeline {
    agent any

    stages {
        stage('execute shell script') {
            steps {
                echo 'executing shell script'
                sh 'chmod +x timestamp.sh'
                sh './timestamp.sh'
            }
        }
    }

    post{
        always {  
             echo 'sending email'  
             emailext body: 'Jenkins Notifications',
                      subject: 'Jenkins Task2 Notification',
                      to: 'aayushkumar3108@gmail.com yugandhara.g@cyware.com'
         } 
    }
}