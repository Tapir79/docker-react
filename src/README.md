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