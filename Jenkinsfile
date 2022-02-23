pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
           echo "build success"
      }
    }
    stage('Test') {
      steps {
          echo "mvn test starts"
      }
    }
    stage('Deploy Development') {
      steps {
            bat "mvn clean package deploy -DmuleVersion=4.4.0 -Dusername=sumedha_March -Dpassword=Lambda=mc2  -DapplicationName=New-prc-api -Denvironment=Sandbox -Dworkers=1 -DworkerType=Micro -Danypoint.platform.client_id=${anypoint_platform_client_id}  -Danypoint.platform.client_secret=${anypoint_platform_client_secret} -Dmule.key=mulesoft -DmuleDeploy"
            echo "deploy success"
      }
    }
  }
}