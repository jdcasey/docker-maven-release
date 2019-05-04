pipeline {
  agent {
    docker {
      image 'fedora'
    }

  }
  stages {
    stage('first-stage') {
      steps {
        node(label: 'maven-release-build') {
          openshiftImageStream(name: 'maven-release', tag: 'latest', namespace: 'Commonjava')
        }

      }
    }
  }
}