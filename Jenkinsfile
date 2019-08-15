pipeline {
  agent any
  stages {
    stage('hello world') {
      steps {
        echo 'hi'
      }
    }
    stage('ec2 part1') {
      steps {
        cfnUpdate(create: true, stack: 'udagram', file: 'udagram.yml', paramsFile: 'udagramdef.json')
      }
    }
    stage('ec2 part2') {
      steps {
        cfnUpdate(stack: 'udagramroute', file: 'udagramrout.yml', paramsFile: 'udagramroutedef.json')
      }
    }
  }
}