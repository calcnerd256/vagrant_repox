copy my-vars.default.yml to my-vars.yml and modify the latter

To run repox:
* check out this repository
* copy ./ansible/my-vars.default.yml onto ./ansible/my-vars.yml
* make sure nothing is listening on port 8080
* run vagrant up
* then open localhost:8080 in a web browser
* log in with username "admin" and password also "admin"
