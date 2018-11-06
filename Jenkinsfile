node("agent1"){
  def mvnHome = tool name: 'maven360' , type:'maven'
  stage('Checkout'){
    git credentialsId: 'githubaccount', url: 'https://github.com/tkkhadka/first.git'

  }
  stage('Execute Test Case'){
    echo "Executing Test Cases"
    sh "${mvnHome}/bin/mvn clean test"
  
  }
  stage('Build'){
    echo "Bulding the job now"
    sh "${mvnHome}/bin/mvn clean package"

  }
  stage('Pst Build Action'){
    echo "Sending an Email to user"
  }
}
