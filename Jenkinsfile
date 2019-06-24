import groovy.json.JsonSlurper
pipeline{  
  agent {label 'slave_ram'}
  stages{
     stage('Pre-Build Installation')
      {
        steps
        {
	 
	 sh "echo 'Installing The Required Packages...'"
         sh 'sudo apt update'
	 sh 'sudo apt install default-jdk'
        }
      } 
      stage('Build')
      {
        steps
        { 

        sh "echo 'shell scripts to build project...'"
		sh 'cd android && ./gradlew assembleDebug'

        }   
      }
     
   }
  }
