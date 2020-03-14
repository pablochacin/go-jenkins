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
             sh 'go build'
          }
         
       }
       stage('test'){
           steps {
               sh 'go test ./...'
            }
       }
       stage('relase') {
          environment {
             GITHUB_TOKEN = credentials(github_token)
          }
          steps {
             sh 'curl -sL https://git.io/goreleaser | bash'
          }
       }
   }
}
     
