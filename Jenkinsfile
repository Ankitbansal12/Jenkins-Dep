#!groovy
import groovy.json.JsonSlurperClassic
node {

    def antVersion = 'Ant'

    stage('checkout source') {
        // when running in multi-branch job, one must issue this command
        checkout scm
    }
	stage('ANT')
	{
    withEnv( ["ANT_HOME=${tool antVersion}"] ) {
    bat '%ANT_HOME%/bin/ant.bat build.xml builderWithGitDiff'
    }
    
            printf rmsg
            println('Hello from a Job DSL script!')
            println(rmsg)
    }
	}
