
properties([
  parameters([
    [$class: 'BuildSelectorParameter', defaultSelector: lastSuccessful(), description: 'Last Successful build', name: 'LAST_SUCCESSFUL_BUILD'],
	booleanParam (name: 'RUN_BUILD', defaultValue: true,
                description: "Run build."),
	booleanParam (name: 'DEPLOY_VAULT_AND_RUN_REGRESSION_TEST', defaultValue: true,
                description: "Run test."),
	string (name: 'BUILD_NUMBER_TO_USE', defaultValue: 'Last Successful build',
                description: 'Build number to use if Build stage is skipped. Default uses Last successful build'),
	string (name: 'TFSBUILDTYPE', defaultValue: 'NightlyLite',
                choices: 'NightlyLite\nNightlyFull',
                description: "Deprecated build type")
  ])
])

node {       
		stage ('Build') {
		}
		
		stage ('Test') {
		}
}
