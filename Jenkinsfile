pipeline {
    agent any
    
    stages {
        stage('removing old soft') {
            steps {
                sh ' sudo yum remove httpd -y '
                sh ' sudo rm -rf /var/www/html'
                   }
                                    }
       stage('installing web server') {
           steps {
                           sh ' sudo yum install httpd -y '
                      }
                                   }
        stage('starting service') {
             steps {
               sh ' sudo systemctl start httpd '
                      }
			}
           stage('deploying web') {
	steps {
                sh ' sudo git clone https://github.com/ashwindevop/myweb1may.git  /var/www/html'
                     }
                                                  }
    }
}
