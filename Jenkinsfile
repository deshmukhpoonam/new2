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
	  sh "docker run -itdp 87:80 --name server1 httpd"
	  sh "cp /mnt/newhttpd/index.html server1:/usr/local/apache2/htdocs"
	}
    }
  }
}
