pipeline {
  agent any
  parameters {
      choice(name: 'VERSION', choices: ['1.1.0', '1.2.0', '1.3.0'], description: '')
      booleanParam(name: 'executeTests', defaultValue: true, description: '')
  }
  stages{
    stage('build') {
      steps {
          echo 'We are builing files here'
      }
    }
    stage('test') {
      when {
        expression {
            params.executeTests
        }
      }
      steps {
          echo 'We are testing files here'
        }
    }
    stage('deploy') {
      steps {
          echo 'We are builing files here'
          echo "depoying version ${params.VERSION}"
        }
    }
  }
}
