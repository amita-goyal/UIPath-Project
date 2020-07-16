pipeline {
  agent any
  stages {
    stage('Git Pull') {
      steps {
        build 'RunDevelopmentProject'
      }
    }

    stage('UIPathWebTests') {
      parallel {
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

    stage('Performance') {
      steps {
        build 'UiPathPerformance'
      }
    }

  }
}