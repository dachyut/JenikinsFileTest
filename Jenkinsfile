
properties([
  parameters([
    choice(choices: ['Branding', 'Non-Branding'], description: 'Build with branding or without branding', name: 'Build'),[$class: 'BuildSelectorParameter', defaultSelector: lastSuccessful(), description: 'Last Successful build', name: 'LAST_SUCCESSFUL_BUILD'],	
	string (name: 'BUILD_NUMBER_TO_USE', defaultValue: 'Last Successful build',
                description: 'Build number to use if Build stage is skipped. Default uses Last successful build')	
  ])
])

node {       
		stage ('Build') {
		}
		
		stage ('Test') {
		}
}
