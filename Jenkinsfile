pipeline {
  agent any
	properties([
  pipelineTriggers([
    upstream(
      threshold: 'SUCCESS',    
      upstreamProjects: '../Multistream/main'
    echo 'This is Branch pipeline-triggers-upstream executed' 
    )
  ])
])
