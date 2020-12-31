pipeline{
	agent any
	stages{
		stage (parameters) { 
			steps{
				script {
                    def INPUT_PARAMS = input message: 'Insira a nova versão do POM', ok: 'Next',
                        
							parameters: [
                            string (name: 'Nova_versão_pom', string: [''].join('\n'), description: '2.xx.0.ATUAL+1-squad_sprint_ATUAL-SNAPSHOT')]
						
						echo  ${Nova_versão_pom}
                    }
				echo  ${"INPUT_PARAMS.Nova_versão_pom"}
			}

		}
		


	}
}