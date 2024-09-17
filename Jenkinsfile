job('Building Docker Files') {
  scm {
    git('https://github.com/nickkostov/project-repo-template.git')
  }
  steps {
    shell('docker build test-image:latest .')
  }
}
