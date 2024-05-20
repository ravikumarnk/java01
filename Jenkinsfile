
pipeline 
{
    agent any

    stages 
	{
	       	stage('Test') 
        	{
         		steps
          		{
			 
                	echo 'Testing my app'
          		}
        	}
	
		stage('Build') 
        	{
         		steps
          		{
			
			 
                	echo 'Building my app'
          		}
        	}

		stage('deploy') 
        	{
         		steps
          		{
			 
                	echo 'Deploy my app'
          		}
        	}
        	
    }
    post
    {
        always
        {
            	emailext body: 'here is th body', subject: 'error', to: 'ravikelakam@gmail.com'
		echo 'Deployment completed..  my app'
        }
        
    }
    
    
}
