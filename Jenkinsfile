pipeline {
  agent any
  stages {
//     stage('git-clone') {
//       steps {
//          bat '''
//          git clone https://github.com/sreekanth-07/samplecheck.git
//          '''
//           }
//      }
      stage("git-push") {
               steps {
	       		withCredentials([gitUsernamePassword(credentialsId: 'sreekanth-jenkins-git', gitToolName: 'Default')]) {
           
                    bat '''
		             // git config --global user.email "kallepusreekanth7@gmail.com"
                             // git config --global user.name "sreekanthtsb"
		     
			     // cd C:\\Users\\002XJB744\\Documents\\check
		             git branch -a
		            
			     git add .
			     git status
	                    
                             git commit -m "update changes"
		             git pull
		            git push -u origin master
		     
	               '''
		   }
        }
    
  }
}
}

