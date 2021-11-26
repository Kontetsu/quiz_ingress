pipeline{

	agent any

	stages {
		stage ('Kubernetis deploy'){
			steps {
					sh ("/usr/local/bin/kubectl -n testenv apply -f ingress.yaml")
				
			}
		}
	}

}

