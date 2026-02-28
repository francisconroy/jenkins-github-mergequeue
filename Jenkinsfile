pipeline {
    agent {
        label 'linux'
    }
    
    stages {
        stage('Build') {
            when {
                not {
                    branch 'main'
                }
            }
            steps {
                echo 'Running build step on change request or branch (not on main)'
            }
        }
    }
}
