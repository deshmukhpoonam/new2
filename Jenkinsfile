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
	  sh "docker run -itdp 90:80 --name server15 httpd"
	  sh "cp /mnt/project/index.html server15:/usr/local/apache2/htdocs"
	  sh "chmod -R 777 /mnt/project/index.html"
	}
    }
  }
}
