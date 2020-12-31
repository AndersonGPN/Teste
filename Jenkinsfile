pipeline {

    agent any

    stages {

        stage("Interactive_Input") {
            steps {
                script {

                    // Variables for input
                    def inputConfig

                    // Get the input
                    def resultParam = input(
                            id: 'resultParam',
							message: 'Insira a nova versão do POM:?',
                            parameters: [

                                    string(defaultValue: 'None',
                                            description: '2.xx.0.ATUAL+1-squad_sprint_ATUAL-SNAPSHOT',
                                            name: 'nova_verso_pom'),
                            ])

                    // Save to variables. Default to empty string if not found.
                    inputConfig = resultParam.nova_verso_pom?:''

                    // Echo to console
                    echo("IQA Sheet Path: ${inputConfig}")
                }
            }
        }
    }
}