pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                // 使用构建工具（如Maven、Gradle等）进行构建
                sh 'echo "Building the application..."'
            }
        }

        stage('Deploy') {
            steps {
                // 使用部署工具（如Ansible、Kubernetes等）进行部署
                sh 'echo "Deploying the application..."'
            }
        }

        stage('Test') {
            steps {
                // 使用测试工具（如JUnit、pytest等）进行测试
                sh 'echo "Testing the application..."'
            }
        }
    }

    post {
        always {
            // 发送构建结果（邮件、钉钉消息等）
            mail to: 'jx6198@buaa.edu.cn',
                 subject: "Jenkins Pipeline: ${currentBuild.fullDisplayName}",
                 body: "Pipeline build result: ${currentBuild.result}"
        }
    }
}
