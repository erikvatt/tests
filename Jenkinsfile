#!/usr/bin/env groovy
pipeline {
  agent any
  when {
    buildingTag()
  }
  stages {
    stage("Clone") {
      steps {
        git(url: "https://github.com/erikvatt/tests.git",
            changelog: false)
      }
    }
  }

  post {
    always {
        deleteDir()
    }
  }
}