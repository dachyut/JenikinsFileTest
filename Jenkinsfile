
properties([
  parameters([
	booleanParam (name: 'RUN_BUILD', defaultValue: true, description: "Run Build"),
    choice(choices: ['Branding', 'Non-Branding'], description: 'Build with branding or without branding', name: 'BUILD_WITH'),
	booleanParam (name: 'RUN_TEST', defaultValue: true, description: "Run Deploy, Smoke and Regression tests"),
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
