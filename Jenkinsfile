pipeline {
    agent any
    stages {
        stage('Git-Checkout'){
            steps {
                echo "Checking out from Git Repo";
                git 'https://github.com/kmp59/PipeLineScripts.git'
            }
        }
        stage('Build'){
            steps {
                echo "Building the checked-out project";
            }
        }
        stage('Quality-Gate') {
            steps{
                echo "verifying quality gates";
            }
        }
        stage('Deploy') {
            steps {
                echo "Deploying to stage environment for more tests!";
            }
        }
    }
    post {
        always {
            echo 'This will always run'
        }
        success {
            echo 'This will run only if successful'
        }
        failure {
            echo 'This will run only if failed'
        }
        unstable {
            echo 'This will run only if the run was marked as unstable'
        }
        changed {
            echo 'This will run only if the state of the Pipeline has changed'
            echo 'For example, if the pipeline was previously failing but is now successful'
        }
    }
}
