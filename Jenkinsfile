node {


	stage 'checkout'
	git url: 'https://github.com/parthodas/dev-ops.git'


        stage 'build'
        workspace = pwd()
        sh "/usr/local/bin/ant jar"

        stage 'test'
        workspace = pwd()
        sh "/usr/local/bin/ant test"
        sh "/usr/local/bin/ant test-report"

        stage 'report'
        workspace = pwd()
        publishHTML (target : [allowMissing: false,
          alwaysLinkToLastBuild: true,
          keepAll: true,
          reportDir: 'build/test/html',
          reportFiles: 'index.html',
          reportName: 'Build Report',
          reportTitles: 'Results'])
        



}
