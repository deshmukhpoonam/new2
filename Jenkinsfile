pipeline {
  agent {
   label {
      label "built-in"
	  customWorkspace "/mnt/project"
        }
	}

 stages {
  stage ("deploy-on-doc-con"){
    steps {
	  sh "docker run -itdp 93:80 --name server25 httpd"
	  sh "docker cp /mnt/project/index.html server25:/usr/local/apache2/htdocs"
	  sh "chmod -R 777 /mnt/project/index.html"
	 
	}
    }
  }
}
