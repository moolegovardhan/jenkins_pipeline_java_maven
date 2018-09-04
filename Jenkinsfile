node{
   stage('SCM Checkout'){
     git 'https://github.com/moolegovardhan/SampleProject'
   }
   stage('Build'){
      // Get maven home path
      def mvnHome =  tool name: 'Maven', type: 'maven'   
      bat "${mvnHome}/bin/mvn -Dmaven.test.failure.ignore clean package"
   step([$class: 'JUnitResultArchiver', testResults: '**/target/surefire-reports/TEST-*.xml'])
   }
}
