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
	  sh "docker run -itdp 91:80 --name server20 httpd"
	  sh "cp -r /mnt/project/index.html server20:/usr/local/apache2/htdocs"
	  sh "chmod -R 777 /mnt/project/index.html"
	}
    }
  }
}
