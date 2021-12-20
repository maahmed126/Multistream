pipeline {
  agent any
	properties([
  pipelineTriggers([
    upstream(
      threshold: 'SUCCESS',    
      upstreamProjects: '../Multistream/main' 
    )
  ])
])
 stages {			
        stage('Build') {			
            steps {			
               echo 'This is branch pipeline-triggers-upstream executed'			
            }			
        }			
    }
}
