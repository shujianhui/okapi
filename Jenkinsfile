#!/usr/bin/groovy

@Library('folio_jenkins_shared_libs@folio-886') _

buildMvn {
  publishModDescriptor = 'no'
  publishAPI = 'yes'
  mvnDeploy = 'yes'

  doDocker = { 
    buildJavaDocker {
      dockerDir = 'okapi-core'
      baseImage = 'folioci/openjdk8-jre-alpine'
      overrideConfig  = 'yes'
      publishMaster = 'no'
    }
  }
}

