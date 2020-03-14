pipeline {
   agent any
   environment {
      GO111MODULES = "on"
   }
   tools {
      go 'go1.14'
   }
   stages {
      stage ('build') {
          steps {
             go 'build'
          }
      }
   }
}
     