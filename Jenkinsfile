pipeline {
    agent any

    environment {
        // Aqui o Jenkins busca no "cofre" e injeta na variável de ambiente
        MINHA_SENHA = credentials('meu-segredo-teste')
    }

    stages {
        stage('Login Externo') {
            steps {
                echo "Iniciando processo de autenticação..."
                
                // O Jenkins é inteligente: ele vai mascarar a senha nos logs com ****
                sh "echo 'Tentando logar com a senha: ${MINHA_SENHA}'"
            }
        }
        
        stage('Deploy simulado') {
            steps {
                echo "Conectando ao ambiente de produção..."
                // Aqui você usaria a variável em comandos reais de AWS ou SSH
            }
        }
    }
}
