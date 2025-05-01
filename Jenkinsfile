pipeline {
    agent any // Визначає, на якому агенті (вузлі Jenkins) буде виконуватися пайплайн

    stages {
        stage('Checkout') {
            steps {
                // Крок для отримання коду з системи контролю версій (наприклад, Git)
                checkout scm
            }
        }
        stage('Build') {
            steps {
                // Кроки для збірки вашого проєкту (наприклад, компіляція Java, Node.js тощо)
                sh 'echo "Building the project..."'
                // Замініть наступну команду на фактичну команду збірки
                // sh './mvnw clean install'
                // sh 'npm install && npm run build'
            }
        }
        stage('Test') {
            steps {
                // Кроки для виконання тестів
                sh 'echo "Running tests..."'
                // Замініть наступну команду на фактичну команду запуску тестів
                // sh './mvnw test'
                // sh 'npm run test'
                junit 'target/surefire-reports/*.xml' // Для відображення результатів JUnit
            }
        }
        stage('Package') {
            steps {
                // Кроки для пакування вашого застосунку (наприклад, створення JAR, WAR, Docker-образу)
                sh 'echo "Packaging the application..."'
                // Замініть наступну команду на фактичну команду пакування
                // sh './mvnw package'
                // sh 'docker build -t my-app .'
            }
        }
        stage('Deploy') {
            steps {
                // Кроки для розгортання вашого застосунку
                sh 'echo "Deploying the application..."'
                // Замініть наступні команди на фактичні команди розгортання
                // sh 'scp target/my-app.jar user@remote:/opt/app/'
                // sh 'kubectl apply -f deployment.yaml'
            }
        }
    }
}
