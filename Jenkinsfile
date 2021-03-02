pipeline {
     agent any
     stages {
         stage('Build') {
             steps {
                 echo 'Building...'
             }
             post {
                 always {
                     jiraSendBuildInfo site: 'fresco3.atlassian.net', branch: 'TDB-2_main'
                      
                 }
             }
         }
     }
 }
