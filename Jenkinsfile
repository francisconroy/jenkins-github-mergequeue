pipeline {
    agent {
        label 'linux'
    }
    
    stages {
        stage('Build') {
            when {
                anyOf {
                    not {
                        branch 'main'
                    }
                    changeRequest()
                }
            }
            steps {
                echo 'Running build step on change request or branch (not on main)'
				echo 'Here\'s another little change for us to use to validate'
				echo 'Yet another test'
            }
        }
    }
}
