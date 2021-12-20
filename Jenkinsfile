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
