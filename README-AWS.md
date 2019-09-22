# Elastic beanstalk 
* Create new application container              
  ** name: 'docker-react'       
  ** Create    
* Create an environment inside the container (create one now)                
  ** Web server environment
     *** Base configuration/ Platform / Docker
     *** Application code / Sample application 

* Create new IAM user 
  ** User name: docker-react-travis-ci
  ** Access type: Programmatic access
  ** Attach existing policies directly -> beanstalk -> provide full acces 
  ** Tags: null
  ** Review : Create user 
  Save secret access key (only shown this 1 time)

  * Travis secret
    ** Dashboard / More options / Settings / Environment variables 
       Access key ID / Secret Access key ID

  * Add deploy options to travis file