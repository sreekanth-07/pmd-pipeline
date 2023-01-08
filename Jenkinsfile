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
	       		
           
                    bat '''
		              
			     echo 'test' >> sample.properties
		             git checkout main
		            
			     git add .
			     git status
	                    
                             git commit -m "update changes"
		             git pull
		            git push https://github.com/sreekanth-07/pmd-pipeline.git main
		     
	               '''
		   
        }
    
  }
}
}

