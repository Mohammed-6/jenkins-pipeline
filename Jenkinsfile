pipeline {
    agent any
    stages {
        stage('Example') {
            steps {
                echo "Running ${env.BUILD_ID} on ${env.JENKINS_URL}"
                echo "Branch Name ${env.BRANCH_NAME}"
                echo "Is Branch Primary ${env.BRANCH_IS_PRIMARY}"
                echo "Change ID ${env.CHANGE_ID}"
                echo "Change URL ${env.CHANGE_URL}"
                echo "Change title ${env.CHANGE_TITLE}"
                echo "Build tag jenkins-${env.JOB_NAME}-${env.BUILD_NUMBER}"
                echo "Build url ${env.BUILD_URL}"
                echo "Executor Number ${env.EXECUTOR_NUMBER}"
                echo "Java Home ${env.JAVA_HOME}"
                echo "Jenkins URL ${env.JENKINS_URL}"
                echo "Job Name ${env.JOB_NAME}"
                echo "Node Name ${env.NODE_NAME}"
                echo "Workspace ${env.WORKSPACE}"
            }
        }
    }
}
