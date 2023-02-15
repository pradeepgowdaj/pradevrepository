pipeline {
    agent any 
    stages {
        stage ("1. install ansible pkg") {
            steps {
                sh "sudo amazon-linux-extras install -y ansible2"
                sh "mkdir -p inbound"
                sh "mkdir -p outbound"
            }
        }
         stage ("2. service install") {
            steps {
                sh "sudo yum update -y"
                sh "sudo yum install -y docker"
            }
        }
        stage ("3. service start") {
            steps {
                sh "sudo systemctl restart docker"
                sh "sudo systemctl enable docker"
            }
        }
        stage ("4. ansible") {
            steps {
                sh "ansible --version"
                sh "rpm -qa | grep ansible"
            }
        }
        stage ("5. create file") {
            steps {
                sh "echo test.txt"
                sh "date"
                sh "cal"
            }
        }
        stage ("6. add uptime") {
            steps {
                sh "echo test1.txt"
                sh "date"
                sh "cal"
            }
        }
        stage ("7. get inside folder") {
	    steps {
	            sh "sudo chmod -R 777 /var/www/html/"
                sh "cd /var/www/html/"
                writeFile(file: "/var/www/html/index.html", text: "this is besant website", encoding: "UTF-8") 
	     }
        } 	
    }
}



