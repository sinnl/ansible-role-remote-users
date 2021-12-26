remote_users
=========

Creates and configures remote users with full sudo option.

Role's Variables
-----------------
- Automation User's Dictionary

  ```
  automation_users:
    XXXXXXX:            # username to create
      pass_hash: ''     # password hash
      uid: ''           # UID
      home: ''          # home directory path
      comment: ''       # GECOS
      sudoers_file: ''  # path to suders file e. g. /etc/sudoers.d/username
      pub_key: ''       # name of the public key template file in files folder
    YYYYYYYY:           # username to create
      pass_hash: ''     # password hash
      uid: ''           # UID
      home: ''          # home directory path
      comment: ''       # GECOS
      sudoers_file: ''  # path to suders file e. g. /etc/sudoers.d/username
      pub_key: ''       # name of the pub key.
  ```

- public key files:
  - need to be present in $HOME/ssh_public_keys directory
  - named same as pub_key value from Automation User's dictionary.

Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

    - hosts: servers
      roles:
         - { role: sinnl.remote_users }

License
-------

BSD

Author Information
------------------

Lukasz
