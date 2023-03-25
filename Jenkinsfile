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
	  sh "docker run -itdp 88:80 --name server11 httpd"
	  sh "cp /mnt/newhttpd/index.html server11:/usr/local/apache2/htdocs"
	}
    }
  }
}
