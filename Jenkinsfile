pipeline {
  agent any
  stages {
    stage('Git Pull') {
      steps {
        build 'RunDevelopmentProject'
      }
    }

    stage('UIPathWebTests') {
      steps {
        build 'UIPathWebTestOnPremise'
      }
    }

    stage('UIPathAPITests') {
      steps {
        build 'UIPathAPITestOnPremise'
      }
    }

  }
}