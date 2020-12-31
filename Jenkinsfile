pipeline{
	agent any
	stages{
		stage (parameters) { 
			steps{
				script {
                    def resultParam = input (
						id: "Insira",
						message: 'Insira a nova versão do POM',                        
							parameters: [
								string (name: 'Nova_versão_pom', 
								string: [''].join('\n'), 
								description: '2.xx.0.ATUAL+1-squad_sprint_ATUAL-SNAPSHOT'
								)
							]
						)						
                    }
					println resultParam
			}
		}
	}
}