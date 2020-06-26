//this is sample file
pipelineJob('Code-COmpile') {  
  configure { flowdefinition ->    
    flowdefinition << delegate.'definition'(class:'org.jenkinsci.plugins.workflow.cps.CpsScmFlowDefinition',plugin:'workflow-cps') {      
      'scm'(class:'hudson.plugins.git.GitSCM',plugin:'git') {        
        'configVersion'(2)        
        'userRemoteConfigs' {          
          'hudson.plugins.git.UserRemoteConfig' {            
            'url'('https://github.com/Varalakshmi13/jenkins-jobs.git')
            
          }
          
        }
        
        'branches' {
          
          'hudson.plugins.git.BranchSpec' {
            
            'name'('*/master')
            
          }
          
        }
        
        'doGenerateSubmoduleConfigurations'(false)
        
        'submoduleCfg'(class:'list')
        
        'extensions'()
        
      }
      
      'scriptPath'('compile.Jenkinsfile')
      
      'lightweight'(true)
      
    }
    
  }
  
}