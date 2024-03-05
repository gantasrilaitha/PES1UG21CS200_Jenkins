pipeline{
  agent any
  stages{
    stage('Build'){
      steps{
        build 'PES1UG21CS200-1'
        sh 'g++ new.cpp -o output'
        //sh 'mvn clean install'
        //echo 'Build Stage Successful'
      }
    }
    stage('Test'){
      steps{
        sh './output'
        // sh 'mvn test'
        // echo 'Test Stage Successful'
        // post{
        //   always{
        //     juint 'target/surefire-reports/*.xml'
        //   }
        // }
      }
    }
    stage('Deploy'){
      steps{
        //sh 'mvn deploy'
        echo 'Deployment Successful'
      }
    }
  }
  post{
    failure{
      echo 'Pipeline failed'
    }
  }
}
