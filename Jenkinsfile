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
			      git pull
			      echo 'india' >> sample.properties
		              dir
			     git branch 
	                     git status
	                     git add .
                             git status
			    git commit -m "update changes"
			   
			    git push https://github.com/sreekanth-07/pmd-pipeline.git main
		     
	               '''
		   
        }
    
  }
}
}

