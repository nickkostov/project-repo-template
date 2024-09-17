job("Building Docker File") {
	description("This is a Hello World proof of concept (POC) Jenkins job.")
	keepDependencies(false)
	scm {
		git {
			remote {
				github("git@github.com:nickkostov/project-repo-template.git", "ssh")
				credentials("git-ecdsa")
			}
			branch("master")
		}
	}
	disabled(false)
	concurrentBuild(false)
	steps {
		shell('docker build test-image:latest .')
	}
	wrappers {
		preBuildCleanup {
			deleteDirectories(false)
			cleanupParameter()
		}
	}
	configure {
		it / 'properties' / 'jenkins.model.BuildDiscarderProperty' {
			strategy {
				'daysToKeep'('30')
				'numToKeep'('10')
				'artifactDaysToKeep'('-1')
				'artifactNumToKeep'('5')
			}
		}
	}
}
