 node(label) {
	
     def GIT_URL_VALIDATE = 'http://gitlab.ethan.svc.cluster.local:8084/gitlab/root/sfdc_validation.git'
	 def GIT_URL_TOOLS = 'http://gitlab.ethan.svc.cluster.local:8084/gitlab/root/sfdc_cartridge.git'
	 def GIT_URL_NOVASUITE = 'http://gitlab.ethan.svc.cluster.local:8084/gitlab/root/sfdc_novasuite.git'
	 def GIT_CREDENTIAL_ID = 'gitlab'
	 def GIT_BRANCH='master'
      
	stage('Git Checkout') {
            
		 git branch: GIT_BRANCH ,url: GIT_URL_VALIDATE ,credentialsId: GIT_CREDENTIAL_ID
		}			
		dir ('.sfdc-devops-tools'){
            git branch: GIT_BRANCH ,url: GIT_URL_TOOLS ,credentialsId: GIT_CREDENTIAL_ID
		}
		dir ('NovaCopAutomation'){
            git branch: GIT_BRANCH ,url: GIT_URL_NOVASUITE  ,credentialsId: GIT_CREDENTIAL_ID
		}
