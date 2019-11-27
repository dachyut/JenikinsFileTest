String sectionHeaderStyle = '''
    color: white;
    background: green;
    font-family: Roboto, sans-serif !important;
    padding: 5px;
    text-align: center;
'''

String separatorStyle = '''
    border: 0;
    border-bottom: 1px dashed #ccc;
    background: #999;
'''


properties([
  parameters([
	[
            $class: 'ParameterSeparatorDefinition',
            name: 'FOO_HEADER',
            sectionHeader: 'Foo Parameters',
            separatorStyle: separatorStyle,
            sectionHeaderStyle: sectionHeaderStyle
        ],
        booleanParam(
            name: 'FOO 1'
        ),
        booleanParam(
            name: 'FOO 2'
        ),
        booleanParam(
            name: 'FOO 3'
        ),
	extendedChoice (description: '', multiSelectDelimiter: ',', name: 'build3', quoteValue: false, saveJSONParameterToFile: false, type: 'PT_RADIO', value: 'opt1,opt2,opt3', visibleItemCount: 5), 
	booleanParam (name: 'RUN_BUILD', defaultValue: true, description: "Run Build"),
    choice(choices: ['Branding', 'Non-Branding'], description: 'Build with branding or without branding', name: 'BUILD_WITH'),
	booleanParam (name: 'RUN_TEST', defaultValue: true, description: "Run Deploy, Smoke and Regression tests"),
	string (name: 'BUILD_NUMBER_TO_USE', defaultValue: 'Last Successful build',
                description: 'Build number to use if Build stage is skipped. Default uses Last successful build')	
  ])
])

node {       
		stage ('Build') {
			println "******"
			println params.build3
			println "******"
		}
		
		stage ('Test') {
		}
}
