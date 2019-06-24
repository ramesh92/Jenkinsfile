import groovy.json.JsonSlurper
pipeline{  
  agent {label 'slave_ram'}
  stages{
     stage('Pre-Build Installation')
      {
        steps
        {
	 sh 'sudo rm -rf test-dir'	
         sh 'sudo mkdir test-dir'
		 sh "echo 'Installing The Required Packages...'"
         sh 'sudo apt install -y npm'
         sh 'sudo npm install -g react-native-cli '
         sh 'sudo install nodejs-legacy'
         sh 'npm install'
         sh 'install linuxbrew-wrapper'
         sh 'brew install watchman'
         sh 'install build-essential'
         sh 'install android-tools-adb'
         sh 'mkdir -p ~/.gradle && echo "org.gradle.daemon=false" >> ~/.gradle/gradle.properties ' 
		
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
