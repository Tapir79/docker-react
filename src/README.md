Build dev
*********
docker build -f Dockerfile.dev .

Build run
*********
docker run -p 8080:80 f4d302a7e32a
http://localhost:8080/

Build prod
***********
docker build .

Run dev
***
docker run -p 3000:3000 f9fd616eb3ca
http://localhost:3000

Docker compose run dev
********
docker-compose up
http://localhost:3000

File change detection on Windows
********************************
in .env file 
CHOKIDAR_USEPOLLING=true

Allow Docker shared files and open Firewall port 445

Travis
******
https://travis-ci.org/

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