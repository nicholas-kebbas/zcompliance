Role Name
=========

Basic Role for running tasks on z/OS systems

Requirements
------------
None

Role Variables
--------------
User will need to create and populate hosts file

Dependencies
------------
None

Example Playbook
----------------

1. Create "hosts" file and add host information
2. Run this command `ansible-playbook -i hosts -u <username> --ask-pass zfacts.yml inactivity_timeout.yml password_history.yml password_min.yml zfacts.yml`

License
-------

BSD

Author Information
------------------
Abhishek Bhatt
Archana Yadawa
Jason Kahn
Nick Kebbas
Mohinish Daswani

Technical Mentor
Andrew Hicks




