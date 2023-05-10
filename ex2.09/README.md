Instructions in docker-compose file comments

./database already created if needed

nginx.conf file included even though not explicitly asked

Removed environment variables from Dockerfiles and moved variables to docker-compose.yml

Backend environment added:

environment:
    ..
  - REQUEST_ORIGIN=http://localhost

Frontend environment added:

environment:
    ..
  - REACT_APP_BACKEND_URL=http://localhost/api
