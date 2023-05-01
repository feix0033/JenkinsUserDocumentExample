pipeline {
    // 1. 创建第一个 pipeline
    // agent { docker 'node:6.3' }
    // stages {
    //     stage('build') {
    //         steps {
    //             sh 'npm --version'
    //         }
    //     }
    // }

    // 2. 执行多个步骤(steps)
    // agent any
    // stages {
    //     stage('Build') {
    //         steps {
    //             sh 'echo "Hello World"'
    //             sh '''
    //                 echo "Multiline shell steps works too"
    //                 ls -lah
    //             '''
    //         }
    //     }
    // }

    // 3. 超时 (timeout) 重试 (retry)
    // agent any
    // stages {
    //     stage('Deploy') {
    //         steps {
    //             retry(3) {
    //                 sh './flakey-deploy.sh'
    //             }

    //             timeout(time: 3, unit: 'MINUTES') {
    //                 sh './health-check.sh'
    //             }
    //         }
    //     }
    // }

    //4. 完成时动作(post)
    // agent any
    // stages {
    //     stage('Test') {
    //         steps {
    //             sh 'echo "Fail!"; exit 1'
    //         }
    //     }
    // }
    // post {
    //     always {
    //         echo 'This will always run'
    //     }
    //     success {
    //         echo 'This will run only if successful'
    //     }
    //     failure {
    //         echo 'This will run only if failed'
    //     }
    //     unstable {
    //         echo 'This will run only if the run was marked as unstable'
    //     }
    //     changed {
    //         echo 'This will run only if the state of the Pipeline has changed'
    //         echo 'For example, if the Pipeline was previously failing but is now successful'
    //     }
    // }

    // 5. 定义执行环境
    // https://www.jenkins.io/doc/book/pipeline/syntax#agent
    // agent {
    //     docker { image 'node:7-alpine' }
    // }
    // stages {
    //     stage('Test') {
    //         steps {
    //             sh 'node --version'
    //         }
    //     }
    // }


    // 6. 使用环境变量
    agent any

    environment {
        DISABLE_AUTH = 'true'
        DB_ENGINE    = 'sqlite'
    }

    stages {
        stage('Build') {
            steps {
                sh 'printenv'
            }
        }
    }
}
