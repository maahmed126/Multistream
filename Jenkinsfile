pipeline {			
    agent any			
    triggers {
        upstream(upstreamProjects: 'Multistream/main',threshold: hudson.model.Result.SUCCESS)//UNSTABLE, FAILURE, NOT_BUILT, ABORTED
    }
stages {			
        stage('Build') {			
            steps {			
                echo 'BRANCH pipeline-triggers-upstream executed'			
            }			
        }			
    }			
}		
