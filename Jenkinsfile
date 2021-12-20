pipeline {			
    agent any			
    triggers {
        upstream(upstreamProjects: 'pipeline-triggers-upstream-job1',threshold: hudson.model.Result.SUCCESS)//UNSTABLE, FAILURE, NOT_BUILT, ABORTED
    }			
stages {			
        stage('Build') {			
            steps {			
                echo 'pipeline-triggers-upstream executed'			
            }			
        }			
    }			
}	
