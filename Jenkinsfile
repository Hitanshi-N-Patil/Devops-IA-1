pipeline {
    agent any

    stages {
        stage('Setup Environment') {
            steps {
                sh 'docker-compose -f docker-compose.yml up -d'
            }
        }

        stage('Run Ansible Playbook') {
            steps {
                sh '''
                docker exec ansible-node1 ansible-playbook \
                    -i /ansible/inventory.ini /ansible/playbook.yml
                '''
            }
        }

        stage('Verify Web Servers') {
            steps {
                sh 'curl -s http://localhost:9081 || echo "Node2 not reachable"'
                sh 'curl -s http://localhost:9082 || echo "Node3 not reachable"'
            }
        }
    }

    post {
        always {
            sh 'docker-compose -f docker-compose.yml down'
        }
    }
}
