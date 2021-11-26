pipeline{

	agent any

	stages {
		stage ('Helm deploy'){
			steps {
					sh ("helm repo add ingress-nginx https://kubernetes.github.io/ingress-nginx")
					sh ("helm repo update")
					sh ("helm install ingress-nginx ingress-nginx/ingress-nginx --create-namespace --namespace ingree-basic")
				
			}
		}
		stage ('Kubernetis deploy'){
			steps {
					sh ("/usr/local/bin/kubectl -n testenv apply -f ingress.yaml")
				
			}
		}
	}

}

