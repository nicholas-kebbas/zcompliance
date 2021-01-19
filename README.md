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

Compliance Protocols
--------------------

| Fact | PCI DSS | Short Description | LongDescription | Check |
|-|-|-|-|-|
| `password_history` | 8.2.5 | Specifies the number of previous passwords and password phrases | Specifies the number (1-32) of previous passwords and password phrases that RACF saves for each user and compares it with each new intended value. | 8 or greater |
| `password_interval` | 8.2.4 | Control change intervals for passwords and password phrases | Control change intervals for passwords and password phrases | Less than or equal to 90 |
| `password_minimum_change_interval` | TBD | Specifies the number of days that must pass between a user's password and password phrase changes. | Specifies the number of days that must pass between a user's password and password phrase changes. Acceptable values are 0-254 (days), providing the number of days between changes does not exceed the maximum change interval specified by the INTERVAL keyword. For example, if you specify 5 for your MINCHANGE number, users cannot change their passwords more than once in 5 days, nor can they change their password phrases (if assigned) more than once in 5 days. | 1 |

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




