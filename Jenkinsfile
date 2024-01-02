pipeline {
    agent any

    environment {
        // Define las variables de entorno necesarias
        CI = 'true'
    }

    stages {
        stage('Checkout') {
            steps {
                // Obtener el código fuente del repositoriogfrgf
                checkout scm
            }
        }

        stage('Install Dependencies') {
            steps {
                // Instalar las dependencias de Node.js
                sh 'npm install'
            }
        }

        stage('Build') {
            steps {
                // Construir la aplicación React
                sh 'npm run build'
            }
        }

        stage('Test') {
            steps {
                // Ejecutar pruebas (opcional)
                sh 'npm test'
            }
        }

        // Opcional: Agrega etapas para desplegar tu aplicación
        // stage('Deploy') {
        //     steps {
        //         // Pasos para desplegar la aplicación
        //         // Por ejemplo, puede ser un script de despliegue o comandos adicionales
        //     }
        // }
    }

    post {
        always {
            // Acciones que siempre se ejecutan, como limpieza
            // Ejemplo: Limpiar archivos temporales
        }

        success {
            // Acciones en caso de éxito
            // Ejemplo: Enviar notificaciones de éxito
        }

        failure {
            // Acciones en caso de fallo
            // Ejemplo: Enviar notificaciones de fallo
        }
    }
}
