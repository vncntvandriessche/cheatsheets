# Pass

The standard Unix password manager.

Simple script that manages your passwords using _GnuPG_, basic files/folder structure and optionally _git_.


## Environment variable

> To change the password storage directory to the current one

    export PASSWORD_STORE_DIR="$( pwd )/";


Basically there are 3 options to choose from:

  - DIR
  - KEY
  - GIT

Append *PASSWORD_STORE_* to these, they are self-explanatory.


## Starting

> Generate a GnuPG key

    gpg --gen-key;


> Put the root folder for the password store into 'PASSWORD_STORE_DIR'.

    PASSWORD_STORE_DIR="$( pwd )/";


> Initialize the new password storage. Point replace <gpg-id> with your newly generated gpg key's id.

    pass init <gpg-id>;


> Create your first password.

    pass insert <pass-group>/<pass-name>;


> List passwords.

    pass ls;


> Insert password into paste-buffer.

    pass -c <pass-group>/<pass-name>;
