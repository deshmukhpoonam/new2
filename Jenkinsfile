pipeline {
  agent {
   label {
      label "built-in"
	  customWorkspace "/mnt/newhttpd"
        }
	}

 stages {
  stage ("deploy-on-doc-con"){
    steps {
	  sh "docker run -itdp 86:80 --name server httpd"
	  sh "cp /mnt/newhttpd/index.html server:/usr/local/apache2/htdocs"
	}
    }
  }
}
