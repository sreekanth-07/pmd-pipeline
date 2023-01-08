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
		              
			    
		             git checkout main
			      echo 'test' >> sample.properties
		              dir
			     git branch 
	                     git status
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

