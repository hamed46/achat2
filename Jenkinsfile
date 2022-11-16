pipeline {

      /*agent { label 'maven' } */
    agent any 


    stages {

       stage ('GIT') {
            steps {
               echo "Getting Project from Git"; 
                git branch: "main", 
                    url: "https://github.com/hamed46/Devops-Project.git"
            }
        }


        stage("build package") {
            steps {
              
                sh " mvn -version "
            
                sh "mvn clean package -DskipTests"
                // sh "mvn clean package -DskipTests" pour une machine linux
            }
        }
    }
}
