node
{
    stage('Clone source') {
        git url: 'https://github.com/arunsaxena01/DevOps-Demo-WebApp.git'
      jiraSendBuildInfo branch: 'TDB-1', site: 'fresco3.atlassian.net'
      jiraSendDeploymentInfo environmentId: 'Test', environmentName: 'QA test', environmentType: 'testing', 
        serviceIds: ['http://52.255.157.89:8080/QAWebapp/'], 
        site: 'aksservicedesk.atlassian.net', state: 'successful'
    }
  
}
