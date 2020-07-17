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

        stage('UIPAthAPITest') {
          steps {
            build 'UIPathAPITestOnPremise'
          }
        }

        stage('Performance Scripts') {
          steps {
            build 'UiPathPerformance'
          }
        }

      }
    }

  }
}