pipeline {
    agent any
    stages {
        stage('Example') {            
              input {
				id: "versaoPom",
				message: 'Insira a nova versão do POM',                        
				parameters: [
					[$class: 'StringParameterDefinition', defaultValue: 'None', description: '2.xx.0.ATUAL+1-squad_sprint_ATUAL-SNAPSHOT', name: 'nova_verso_pom']
						]
			}
            steps {
                echo "Hello, ${nova_verso_pom}, nice to meet you."
            }
        }
    }
}