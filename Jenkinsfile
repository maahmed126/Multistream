pipeline {
  agent {
    label 'ecs'
  }
  triggers {
        upstream(upstreamProjects: 'pipeline-triggers-upstream-job1', 			
        threshold: hudson.model.Result.SUCCESS)//UNSTABLE, FAILURE, NOT_BUILT, ABORTED
    }	
  stages {
    stage('Awesomeness') {
      steps {
        echo 'Hello from Jenkins slave!'
        touch test.txt
      }
    }
  }
  
  post {

		always {
		    sh '''pwd
		        touch test.txt
                ls -l'''
            archiveArtifacts artifacts: '**/*.txt', allowEmptyArchive: true, fingerprint: true
		    // s3CopyArtifact buildSelector: lastSuccessful(), excludeFilter: '', filter: 'test.txt', flatten: false, optional: false, projectName: 'ecs-demo-test', target: '/home/jenkins/workspace/ecs-demo-test'
		}
  }

}
