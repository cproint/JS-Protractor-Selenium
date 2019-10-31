pipeline {
    agent any
    
    tools {
        maven 'maven_3.6.1'
    }

    stages {
    
        stage('Initialize and Compile') {
            steps {          	
                echo "The pipeline stage Initialize and Compile completed successfully."
            }
        }


     	stage('Functional Tests') {
	        steps {
	            sauce('923fc3a2-50d8-48b1-b8a1-adba6a7b72fe') {
						sh "protractor conf.js"
						step([$class: 'SauceOnDemandTestPublisher'])    
		            	echo "The pipeline stage Functional Tests completed successfully."                    
	            	}   
	            }
        }

        stage('Clean') {
            steps {
                echo "The pipeline stage Clean completed successfully."
            }
        }
        


    }
    
}
