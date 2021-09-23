node {


	stage 'checkout'
	git url: 'https://github.com/parthodas/dev-ops.git'


        stage 'build'
        workspace = pwd()
        sh "ant jar"

        stage 'test'
        workspace = pwd()
        sh "ant test"



}
