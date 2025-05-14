pipeline{
  agent any
  tools{
    'gradle' 'Gradle'
    'jdk' 'JDK'
  }
  stages{
    stage('Checkout'){
      steps{
        gir barnch:'master',url:'https://github.com/bitcse6c/1BI22CS148-gradle.git'
      }
    }
    stage('Build'){
       steps{
         sh 'gradle build'
       }
    }
    stage('Test'){
      steps{
        sh 'gradle test'
      }
    }
    stage('Run'){
      steps{
        sh 'gradle run'
      }
    }
    post{	
		success{
			echo "Successfull"
		}
		failure{
			echo "Unsuccessfull"
		}
	}
}
        
      
