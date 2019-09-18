node{
   stage('SCM Checkout'){
     git 'https://github.com/moolegovardhan/jenkins-pipeline-cucumber-example.git'
   }
   stage('Compile-Package'){
      //sh 'mvn package'
      def mvnHome =  tool name: 'Maven-3', type: 'maven'   
      sh "${mvnHome}/bin/mvn package"
   }
}
