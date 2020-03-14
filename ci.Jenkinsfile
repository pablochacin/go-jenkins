pipeline {
   agent any
   environment {
      GO111MODULES=on
   }
   stages {
      stage ('build') {
          steps {
             go build
          }
      }
   }
}
     