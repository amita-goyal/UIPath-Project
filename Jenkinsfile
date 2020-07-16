pipeline {
  agent any
  stages {
    stage('Git Pull') {
      steps {
        build 'UIPathWebTestOnPremise'
        build 'RunDevelopmentProject'
      }
    }

  }
}