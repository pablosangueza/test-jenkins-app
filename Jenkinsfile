pipeline {
  agent any
 environment 
 {
      SAY_HELLO="hola Mundo"		
 }
 stages {
        stage('Preparation') {
            steps {
                echo 'Preparation...'
                script {
                    checkout scm
					          sh '''
                        chmod 755 -R ./ 
                    '''
                    echo "${SAY_HELLO}"
                   
                }

            }
        }
  }
  post
	{
		cleanup
		{
			script
			{
				echo "clean all"
			}
		}
	}
 

}
