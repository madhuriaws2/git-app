pipeline {
	agent {
		node {
			label 'built-in'
			customWorkspace '/mnt/git-app'
		}
	}
stages {
	stage ('install'){
		steps {
				sh "yum install httpd -y"
		}
	}
	stage ('start'){
	    steps {
	            sh "service httpd restart"
	    }
	}
	stage ('echo-message'){
	    steps {
	            sh " cp -r index.html /var/www/html
	            sh "chmod -R 777 /var/www/html/index.html"
	    }
	}
}
}
    
