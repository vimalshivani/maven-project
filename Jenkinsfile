pipeline {
    agent any

   tools {
        maven 'MAVEN'
    } 
     
    

    stages{
        stage('Build'){
            steps{
                 sh  'mvn clean package'
		 sh 'docker build . -t tomcatwebapp:${env.BUILD_ID}'
                //bat "docker build . -t tomcatwebapp:${env.BUILD_ID}"
                //bat "echo ${my_tag}"
            }

        }
    }
}
