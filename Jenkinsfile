pipeline {

    agent any

    stages {

        stage("Interactive_Input") {
            steps {
                script {

                    // Variables for input
                    def inputnova_verso_pom
                    def inputTest

                    // Get the input
                    def resultParam = input(
                            id: 'resultParam', message: 'Enter path of test reports:?',
                            parameters: [

                                    string(defaultValue: 'None',
                                            description: '2.xx.0.ATUAL+1-squad_sprint_ATUAL-SNAPSHOT',
                                            name: 'nova_verso_pom'),
                                    string(defaultValue: '-SNAPSHOT',
                                            description: '-SNAPSHOT',
                                            name: 'Test'),
                            ])

                    // Save to variables. Default to empty string if not found.
                    inputnova_verso_pom = resultParam.nova_verso_pom?:''
                    inputTest = resultParam.Test?:''

                    // Echo to console
                    echo("IQA Sheet Path: ${inputnova_verso_pom}")
                    echo("Test Info file path: ${inputTest}")

                    // Write to file
                    writeFile file: "inputData.txt", text: "nova_verso_pom=${inputnova_verso_pom}${inputTest}"

                    // Archive the file (or whatever you want to do with it)
                    archiveArtifacts 'inputData.txt'
                }
            }
        }
		stage("Ler variavel"){
			steps{
				sh '''
					while read VERSAO_POM; do

					POM ==$(echo $LINHA | awk '{print $1}')

					done < inputData.txt
					echo "nova_verso_pom=${inputnova_verso_pom}"
					cat inputData.txt
						echo $VERSAO_POM
				'''
			}
		}		
    }
}