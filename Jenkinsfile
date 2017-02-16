node {
  gitCommit = sh(returnStdout: true, script: 'git rev-parse HEAD').trim()
  //shortCommit = gitCommit.take(6)
  echo "SHORT gitCommit"
}

runPipeline('githubflow') {
  appName = 'basic-springboot-app'
  role = 'basic-spring'
  platform = 'java'
  cookbookName = 'tc-canary'
  chefRepo {
        uri = 'git@github.com:ThomasCookOnline/chef-repo'
        credentials = '9af674bb-7bea-4eee-9332-17bd93dffb14'
  }

}

