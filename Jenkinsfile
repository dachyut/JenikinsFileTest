
properties([
    parameters([
            string (name: 'TFSBUILDTYPE', defaultValue: 'NightlyLite',
                choices: 'NightlyLite\nNightlyFull',
                description: "Another build type parameter, where 'NightlyLite' goes with BUILD_TYPE FAST and 'NightlyFull' goes with BUILD_TYPE NIGHTLY."),
            string(name: 'LOG_LEVEL_OPTIONS', defaultValue: 'debug',
                choices: 'trace\ndebug\ninfo\nwarning\nerror\ncritical',
                description: 'Amount of verbose-ness to print to the log file. Options include "debug", "info", and "error".'),
            string (name: 'BUILD_LABEL', defaultValue: 'CEB-NewBuild',
                description: 'Builds will run on this Jenkins label.'),
            string (name: 'BUILD_BRAND_INDEX', defaultValue: '0',
                description: "If not blank, the index [0-23] of the one brand you want to build. Only used in non-NIGHTLY builds."),
            string (name: 'TEST_PLATFORM', defaultValue: 'CEB-Client-Automation-Win10-UI',
                description: 'Tests will run in parallel across this comma-delimited list of Jenkins labels.'),
            string (name: 'SMOKE_SUITE', defaultValue: 'suites/CI/smoke.suite'),
            string (name: 'REGRESSION_SUITE', defaultValue: 'suites/CI/regression.suite'),
            booleanParam (name: 'COLLECT_TIMING_DATA', defaultValue: false,
                description: 'If true, collect historical timing data to analyze bottlenecks.'),
            booleanParam (name: 'ARCHIVE_TEST_RESULTS', defaultValue: true,
                description: 'If true, archive the tests results in the automation portal.'),
            booleanParam (name: 'RUN_BUILD', defaultValue: true,
                description: 'If true, run the Build stage.'),
            choice (name: 'BUILD_WITH',
                choices: ['Non-Branding', 'Branding'],
                description: 'Build with branding or without branding'),
            booleanParam (name: 'DEPLOY_VAULT_SMOKE_AND_REGRESSION_TEST', defaultValue: true,
                description: 'If true, Deploys Valut and run Smoke, Regression tests.'),
            string (name: 'BUILD_NUMBER_TO_USE', defaultValue: 'Last Successful build',
                description: 'Build number to use if Build stage is skipped. Default uses Last successful build')
    ]),
    disableConcurrentBuilds(),  // Dont let more than one instance of this pipeline run at a time so we don't freeze out everyone else
    buildDiscarder(logRotator(artifactDaysToKeepStr: '', artifactNumToKeepStr: '', daysToKeepStr: '', numToKeepStr: buildsToKeep)),
    pipelineTriggers([cron(cronString)]),
    [$class: 'WebhookJobProperty', webhooks: [generateCEBWebhook (branchName),
                                              generateBB8Webhook (branchName)] ]
])

node {       
		stage ('Build') {
			if (params.BUILD_WITH == 'Branding') {
				currentBuild.description = "Branding"
			}
			else {
				currentBuild.description = "Non-Branding"
			}			
		}
		
		stage ('Deploy Vault') {
			
		}
		
		stage ('Smoke Test') {
		}
		
		stage ('Regression Test') {
		}
}
