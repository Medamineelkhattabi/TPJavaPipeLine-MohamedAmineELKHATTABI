pipeline {
    agent {
        docker {
            // Image contenant Maven et Git
            image 'my-maven-git:latest'
            // Pour réutiliser le cache Maven local entre builds
            args '-v $HOME/.m2:/root/.m2'
        }
    }

    stages {
        stage('Checkout') {
            steps {
                echo "🔄 Checkout du dépôt GitHub"
                // Nettoyer le workspace
                sh 'rm -rf *'
                // Cloner ton dépôt
                sh 'git clone https://github.com/Medamineelkhattabi/TPJavaPipeLine-MohamedAmineELKHATTABI.git .'
            }
        }

        stage('Build & Test') {
            steps {
                echo "🔨 Build et tests Maven"
                script {
                    // Vérifier où on se trouve
                    def currentDir = pwd()
                    echo "📂 Current directory: ${currentDir}"
                    // Exécuter Maven à la racine du dépôt (où est le pom.xml)
                    sh 'mvn clean test package'
                }
            }
        }

        stage('Run') {
            steps {
                echo "▶️ Exécution du jar"
                // Exécuter le jar généré
                sh 'java -jar target/maven-0.0.1-SNAPSHOT.jar'
            }
        }
    }

    post {
        success {
            echo "✅ Pipeline terminé avec succès"
        }
        failure {
            echo "❌ Pipeline échoué"
        }
    }
}
