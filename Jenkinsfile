pipeline {
    agent any

    stages {
        // СТАДИЯ 1: Кодты алу
        stage('Checkout Code') {
            steps {
                echo 'Забираем код из GitHub...'
                checkout scm
            }
        }
        
        // СТАДИЯ 2: Файлдарды тексеру
        stage('Check Files') {
            steps {
                echo ' 📄  Проверяем созданные файлы...'
                sh '''
                    echo "=== ФАЙЛЫ В РЕПОЗИТОРИИ ==="
                    ls -la
                    echo ""
                    echo "=== ПРОВЕРКА НАШИХ ФАЙЛОВ ==="
                    if [ -f Dockerfile ]; then
                        echo "Dockerfile найден"
                    else
                        echo "Dockerfile не найден"
                    fi
                '''
            }
        }
        
        // СТАДИЯ 3: Docker теориясы
        stage('Docker Theory') {
            steps {
                echo 'ТЕОРИЯ DOCKER'
                echo '1. docker build -t my-app .'
                echo '2. docker run -d -p 8081:5000 my-app'
            }
        }
    }
}
