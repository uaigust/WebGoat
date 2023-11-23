
pipeline {
    agent any

    stages {
        stage('Checkmarx Scan') {
            steps {
                node {
                    // Defina os valores necessários para a análise do Checkmarx
                    def checkmarxConfig = [
                        additionalOptions: '', // Opções adicionais, se necessário
                        baseAuthUrl: '', // URL de autenticação, se aplicável
                        branchName: 'main', // Nome da branch a ser verificada
                        checkmarxInstallation: 'Scan', // Nome da instalação Checkmarx no Jenkins
                        credentialsId: 'df4d673f-81b3-4d90-9a68-18107583bced', // ID das credenciais, se necessário
                        projectName: 'teste', // Nome do projeto a ser analisado
                        serverUrl: 'https://108.139.166.40:8080/', // URL do servidor Checkmarx
                        tenantName: 'beta_nova8', // Nome do tenant, se aplicável
                    ]

                    // Execute a etapa checkmarxASTScanner com as configurações definidas acima
                    checkmarxASTScanner(checkmarxConfig)
                }
            }
        }
    }
}
