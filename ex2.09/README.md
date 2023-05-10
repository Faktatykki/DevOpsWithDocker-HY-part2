Instructions in docker-compose file comments

nginx.conf file included even though not explicitly asked

Backend environment added:

environment:

    ..

  - REQUEST_ORIGIN=http://localhost

Frontend environment added:

environment:

    ..

  - REACT_APP_BACKEND_URL=http://localhost/api


Same environment variable changes have been added to Dockerfiles
