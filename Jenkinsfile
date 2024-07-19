pipeline{
  agent any
  parameters{
     choice(name: 'action', choices: 'create\ndelete', description: 'Choose create/Destroy')
  }
  stages{
       stage ('Pushing Jfrog File'){
      when { expression { params.action == 'create' } }
      steps{
        script{
          sh 'curl -X PUT -u admin:Saikrishna@22 -T /opt/git/Java_app_3.0/target/devdemo.jar "http://34.228.161.2:8082/artifactory/example-repo-local/devdemo.jar"'
        }
      }
       }
  }
}
