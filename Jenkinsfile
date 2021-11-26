pipeline{

	agent any

	stages {
		stage ('Helm deploy'){
			steps {
					sh ("/usr/local/bin/helm repo add ingress-nginx https://kubernetes.github.io/ingress-nginx")
					sh ("/usr/local/bin/helm repo update")
					//sh ("/usr/local/bin/helm install ingress-nginx ingress-nginx/ingress-nginx --create-namespace --namespace ingress-basic")
				
			}
		}
		stage ('Kubernetis deploy'){
			steps {
					sh ("/usr/local/bin/kubectl -n testenv apply -f ingress.yaml")
				
			}
		}
	}

}

