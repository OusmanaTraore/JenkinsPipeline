pipeline {
    agent any
    stages {
         stage ('Nettoyage du repertoire') {
            steps {
                //sh " sudo chmod 777 /var/lib/jenkins/workspace/MyPipelines/* "
                sh "  rm -Rf /var/lib/jenkins/workspace/Pipeline1/* " 
            }
         }
            stage ('Clone') {
            steps {
                sh "git clone https://github.com/OusmanaTraore/JenkinsPipeline.git "
            }
        }
        stage ('Build') {
            steps {
                sh "cd /var/lib/jenkins/workspace/Pipeline1/JenkinsPipeline/MvnProject/mon-appli/src/main/java/ && javac org/example/demo/App.java"
           }           
        }
        stage ('Run') {
            steps {
                sh " cd /var/lib/jenkins/workspace/Pipeline1/JenkinsPipeline/MvnProject/mon-appli/src/main/java/  && java org/example/demo/App  "
            }
        }
    }
}
