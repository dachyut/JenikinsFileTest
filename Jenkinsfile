
properties([
  parameters([
		
	booleanParam (name: 'RUN_BUILD', defaultValue: true, description: "Run Build"),
	
	extendedChoice (description: 'Build with branding or without branding', multiSelectDelimiter: ',', name: 'BUILD_WITH', type: 'PT_RADIO', value: 'Branding,Non-Branding', defaultValue: (params.RUN_BUILD)?'Branding':'Non-Branding'),	
    	
	booleanParam (name: 'RUN_TEST', defaultValue: true, description: "Run Deploy, Smoke and Regression tests"),
	
	string (name: 'BUILD_NUMBER_TO_USE', defaultValue: 'Last Successful build',
                description: 'Build number to use if Build stage is skipped. Default uses Last successful build')	
  ])
])

node {       
		stage ('Build') {
			println "******"
			println params.BUILD_WITH
			println "******"
		}
		
		stage ('Test') {
		}
}
