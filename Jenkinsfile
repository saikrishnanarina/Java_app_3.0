pipeline{
  agent jenkins-slave
  parameters{
     choice(name: 'action', choices: 'create\ndelete', description: 'Choose create/Destroy')
  }
  stages{
       stage ('Pushing Jfrog File'){
      when { expression { params.action == 'create' } }
      steps{
        script{
          sh 'curl -X PUT -u admin:Saikrishna@22 -T /opt/pro/krishna/target/narina.jar "http://54.227.190.70:8082/artifactory/example-repo-local/my_pro-docker.jar"'
          //Below command for deleting jar/files/anything in jfrog remote repository
         // sh 'curl -X DELETE -u admin:Saikrishna@22 "http://54.163.211.17:8082/artifactory/example-repo-local/my_pro-docker.jar"'
        }
      }
       }
  }
}
