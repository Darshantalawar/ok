pipeline { 
    agent any 
    tools { 
          maven 'Maven' //Ensure name matches with configured  
    } 
    stages { 
        stage('Checkout') {  
            steps { 
                git branch: 'main', url: ''  
            } 
    } 
     stage('Build') {  
            steps { 
                bat 'mvn clean package'  
            } 
      } 
     stage('Test') {  
            steps { 
                bat 'mvn test'  
            } 
      } 
     stage('Run Application') {  
            steps { 
                bat 'java -jar target/ok-0.0.1-SNAPSHOT.jar'  
            } 
      } 
    } 
}
