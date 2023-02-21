pipeline {
  agent any 
            
  tools {
    maven 'maven'
  }
        
  environment {
    Snyk = 'Snyk'
    Trivy = 'Trivy'
    Audit = 'Audit'
  }
  
  stages {
    stage ('Initialize') {
      steps {
        sh '''
                    echo "PATH = ${PATH}"
                    echo "M2_HOME = ${M2_HOME}"
                  
            ''' 
      }
    } 
    
 
    stage ('Report') {
     steps {
            //sh 'chmod +777 /var/lib/jenkins/workspace/CICD'
            //sh 'sudo cp -r /var/lib/jenkins/workspace/CICD /var/www/html' 
            sh 'sudo cp -r /var/lib/jenkins/workspace/DJScan/./dependency-check-report.html  /var/www/html/DJScan'
       }
    }
      
  }
} 
