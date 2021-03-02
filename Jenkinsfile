pipeline {
     agent any
     stages {
         stage('Build') {
             steps {
                 echo 'Building...'
             }
             post {
                 always {
                     jiraSendBuildInfo site: 'aksservicedesk.atlassian.net',branch: 'JNG-1_main'
                 }
             }
         }
         stage('Deploy - Staging') {
             when {
                 branch 'master'
             }
             steps {
                 echo 'Deploying to Staging from master...'
             }
             post {
                 always {
                     jiraSendDeploymentInfo site: 'aksservicedesk.atlassian.net', environmentId: 'JNG-1', environmentName: 'JNG-1', environmentType: 'staging'
                 }
             }
         }
         stage('Deploy - Production') {
            when {
                branch 'master'
            }
            steps {
                echo 'Deploying to Production from master...'
            }
            post {
                always {
                    jiraSendDeploymentInfo site: 'aksservicedesk.atlassian.net', environmentId: 'JNG-1', environmentName: 'JNG-1', environmentType: 'production'
                }
            }
         }
     }
 }
