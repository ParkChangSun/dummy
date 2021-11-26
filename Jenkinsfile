CODE_CHANGES = getGitChanges()
pipeline{
    
    agent any
    
    stages {
    
        stage("build") {
            when {
                expression {
                    BRANCH_NAME == 'feature/Son' && CODE_CHANGES == true   
                }
            }
      
            steps {
                echo 'building the application...'
            }
        }
        
        stage("test") {
            when {
                expression {
                    BRANCH_NAME == 'feature/Son' || BRANCH_NAME == 'master' 
                }
            }
            
            steps {
                echo 'testing the application...'
            }
        }
        
        stage("deploy") {
            
            steps {
                echo 'deploying the application...'
            }
        }
    }
    post {
        //3 conditions
        always {
            //    
        }
        success {
            //   
        }
        failure {
            //   
        }
    }
}
