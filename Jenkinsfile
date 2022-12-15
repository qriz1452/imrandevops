pipeline {
	agent any
	tools {
		maven "MAVEN3"
		jdk "OracleJDK8"
	}
	encironment {
		SNAP_REPO = 'vpro-artifact-snapshots'
		NEXUS_USER = 'admin'
		NEXUS_PASS = 'admin'
		RELEASE_REPO = 'vpro-artifact-host'
		CENTRAL_REPO = 'vppr-artifact-dependencies'
		NEXUSIP = '172.31.13.211'
		NEXUSPORT = '8081'
		NEXUS_GRP_REPO = 'vpr-artifact-group'
		NEXUS_LOGIN = 'nexuslogin'
	}
	stages {
		stage ('Build') {
			sh 'mvn -s settings.xml -DskipTests install'
		}
	}

}
