node{
   stage('SCM Checkout'){
     git 'https://github.com/moolegovardhan/jenkins-pipeline-cucumber-example.git'
   }
   stage('Compile-Package'){
      // Get maven home path
      def mvnHome =  tool name: 'Maven', type: 'maven'   
      bat "${mvnHome}/bin/mvn package"
   }
}
