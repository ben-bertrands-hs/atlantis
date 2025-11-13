#!groovy

@Library('hootsuite@6') _

gitOpsPipeline {

  agentType = 'go-22-agent'

  container = 'go'

  deployServiceName = 'atlantis-hackathon'

  image {

    name = 'atlantis-hackathon'

    target = 'alpine'

  }

  build = {

    usingECR() {

        usingArtifactoryAPI() {

            sh 'make docker/dev'

        }

    }

  }

  deployStaging = false

  deployProduction = false

}

