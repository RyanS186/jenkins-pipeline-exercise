pipeline{
        agent any
        stages{
            stage('Clone Repo'){
                steps{
                    git branch: '*/main', url: 'https://github.com/RyanS186/jenkins-pipeline-script'
                }
            }
            stage('Run script'){
                steps{
                    sh 'sh ./myscript.sh'
                }
            }
	    stage('Archive file'){
		steps{
		    archiveArtifacts artifacts: 'output', followSymlinks: false
		}
            }
	}
}
