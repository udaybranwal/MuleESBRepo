pipeline
{
  agent any
  stages{
    
    stage('Build Application'){
      steps{
        bat 'mvn clean install'
      }
    }

    stage('Deploy Application To Mulesoft CloudHub'){
      steps{
        bat 'mvn package deploy -DmuleDeploy'
      }
    }
    stage('Perform Regression Testing'){
      steps{
        bat 'C:\\Users\\uday\\AppData\\Roaming\\npm\\newman run E:\\TestTools\\postman\\WorldTimeZone.postman_collection.json --disable-unicode'
      }
    }    
  }	
}