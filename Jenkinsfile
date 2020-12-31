pipeline{
	agent any
	stages{
		stage (parameters) { 
			steps{
				script {
                    def resultParam = input id: 'VersaoPom', 
					message: 'Insira valor', 
					parameters: [string(defaultValue: '', 
					description: '''Será a nova versão do pom
						2.xx.0.ATUAL+1-squad_sprint_ATUAL-SNAPSHOT''', name: 'nova_versao_pom', trim: true)]			
                    }
					println resultParam
			}
		}
	}
}