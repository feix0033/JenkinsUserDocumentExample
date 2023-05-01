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

    /* 4. 完成时动作(post) */ 
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

    /* 5. 定义执行环境 */
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


    /* 6. 使用环境变量 */
    // agent any

    // environment {
    //     DISABLE_AUTH = 'true'
    //     DB_ENGINE    = 'sqlite'
    // }

    // stages {
    //     stage('Build') {
    //         steps {
    //             sh 'printenv' /*输出环境数据 */
    //         }
    //     }
    // }

    /* 7. 输出测试结果 */
//    agent any
//     stages {
//         stage('Build') {
//             steps {
//                 sh 'dotnet build'
//             }
//         }
//         stage('Test') {
//             steps {
//                 sh 'dotnet test'
//             }
//         }
//     }

//     post {
//         always {
            /* 这里通过 archive artifacts 步骤和文件匹配表达式输出记录文件 */
//             archiveArtifacts artifacts: 'build/libs/**/*.jar', fingerprint: true
//      参数:  文件名                           路径                    许可
            /*  这里通过 junit 路径 输出 junit 测试记录 */
//             junit 'build/reports/**/*.xml'
//         }
//     }

    /* 8. 清理和通知 */
    // agent any
    // stages {
    //     stage('No-op') {
    //         steps {
    //             sh 'ls'
    //         }
    //     }
    // }
    // post {
    //     always {
    //         echo 'One way or another, I have finished'
    //         deleteDir() /* clean up our workspace */
    //     }
    //     success {
    //         echo 'I succeeeded!'
    //     }
    //     unstable {
    //         echo 'I am unstable :/'
    //     }
    //     failure {
    //         echo 'I failed :('
    //         /* 发送 email 通知测试失败 */
    //         mail to: 'team@example.com',
    //          subject: "Failed Pipeline: ${currentBuild.fullDisplayName}",
    //          body: "Something is wrong with ${env.BUILD_URL}"
    //     }
    //     changed {
    //         echo 'Things were different before...'
    //     }
    // }

    /* 9. 部署阶段 */
    // agent any
    // stages {
    //     stage('Build') {
    //         steps {
    //             echo 'Building'
    //         }
    //     }
    //     stage('Test') {
    //         steps {
    //             echo 'Testing'
    //         }
    //     }
    //     stage('Deploy') {
    //         steps {
    //             echo 'Deploying'
    //         }
    //     }
    //     /* 这一步是添加人工确认来执行部署 */
    //     stage('Sanity check') {
    //         steps {
    //             input "Does the staging environment look ok?"
    //         }
    //     }
    // }
}