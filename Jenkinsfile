@Library('tomcat-hello-world@master') _

pipeline {
    agent any
    
    tools{
           maven 'apache-maven-3.8.5'
    }

    stages{
        stage('Git Checkout'){
            steps{
                  gitCheckout(
                               branch: "master",
                               url: "https://github.com/harith2207/tomcat-hello-world.git"
                              )
            }
        }
                   
        stage('Hello') {


             steps {


                     sh '''
                             java -version
                         '''


              }


           }
        // Maven compile Stage
        stage ('mvn Build Stage') {
            steps {
                echo "Running the Build"
                sh 'mvn clean install'
            }
        }
        
     }

}
