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
	  sh "docker run -itdp 92:80 --name server22 httpd"
	  sh "docker cp /mnt/project/index.html server22:/usr/local/apache2/htdocs"
	 
	}
    }
  }
}
