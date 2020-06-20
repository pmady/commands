#!/usr/bin/env groovy

def nodes
def versions

node {
   sh 'pwd'
   nodes = sh (script: '../parameters_JenkinsfileParameters@script/list_nodes.sh', returnStdout: true).trim()
}

pipeline {
agent any
    parameters {
            choice(name: 'Invoke_Parameters', choices:"Yes\nNo", description: "Do you whish to do a dry run to grab parameters?" )
            choice(name: 'Nodes', choices:"${nodes}", description: "")
    }
    stages {
        stage("parameterizing") {
            steps {
                script {
                    if ("${params.Invoke_Parameters}" == "Yes") {
                        currentBuild.result = 'ABORTED'
                        error('DRY RUN COMPLETED. JOB PARAMETERIZED.')
                    }
                }
            }
        }
        stage("choose version") {
            steps {
                script {
                    def version_collection
                    def chosen_node = "${params.Nodes}"
                    version_collection = sh (script: "../parameters_JenkinsfileParameters@script/list_versions.sh $chosen_node", returnStdout: true).trim()
                    versions = input message: 'Choose testload version!', ok: 'SET', parameters: [choice(name: 'TESTLOAD_VERSION', choices: "${version_collection}", description: '')]
                }
           }
        }
}

pipeline {
    agent any
    parameters {
        string(name: 'PERSON', defaultValue: 'Mr Jenkins', description: 'Who should I say hello to?')

        text(name: 'BIOGRAPHY', defaultValue: '', description: 'Enter some information about the person')

        booleanParam(name: 'TOGGLE', defaultValue: true, description: 'Toggle this value')

        choice(name: 'CHOICE', choices: ['One', 'Two', 'Three'], description: 'Pick something')

        password(name: 'PASSWORD', defaultValue: 'SECRET', description: 'Enter a password')
        
    }
    stages {
        stage('Example') {
            steps {
                echo "Hello ${params.PERSON}"

                echo "Biography: ${params.BIOGRAPHY}"

                echo "Toggle: ${params.TOGGLE}"

                echo "Choice: ${params.CHOICE}"

                echo "Password: ${params.PASSWORD}"
            }
        }
    }
}
