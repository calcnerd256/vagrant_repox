copy my-vars.default.yml to my-vars.yml and modify the latter

gotchas:
 some ansible variables don't actually support changing at this time
  I'm not sure what db.privileges needs to be
  path.source needs to be a nonexistent immediate subdirectory of an existing directory
  path.data needs to be a nonexistent immediate subdirectory of an existing directory
  path.log needs to be an existing directory
  path.playbook assumes vagrant, so we'll need to adapt to other provisioners
  no path should end with a /
  source_tag must be v3.1.0 or the j2 templates need to change accordingly
  ldap is wrong
  base_urn is wrong
  smtp is wrong

TODO: set up e-mail

To run repox:
* check out this repository
* copy ./ansible/my-vars.default.yml onto ./ansible/my-vars.yml
* make sure nothing is listening on port 8080
* run vagrant up
* then open localhost:8080 in a web browser
* log in with username "admin" and password also "admin"
