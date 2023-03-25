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
	  sh "docker run -itdp 85:80 --name server10 httpd"
	  sh "cp /mnt/project/index.html server10:/usr/local/apache2/htdocs"
	}
    }
  }
}
