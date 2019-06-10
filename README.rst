pgbackup 
======== 

CLI for backing up remote PostgreSQL databases either locally or to S3. 

Preparing the Development 
-------------------------

1. Ensure ``pip`` and ``pipenv`` are installed. 
2. Clone repository: ``git clone git@github.com:nshipman/pgbackup`` 
3. ``cd`` into the repository. 
4. Fetch development dependencies ``make install`` 
5. Activate virtualenv: ``pipenv shell`` 

Usage
-----

Pass in a full database URL, the storage driver and the destination. 

S3 Example: 

:: 

  $ pgbackup postgres://tom@example.com:5432/db_one --driver s3 backups

Local Example: 

:: 
  $ pgbackup postgres://tom@example.com:5432/db_one --driver local /var/local/db_one/backups/dump.sql

Running Tests
-------------

Run tests locally using ``make`` if virtualenv is active: 

:: 

    $ make 

If virtualenv is not active then use: 

:: 

    $ pipenv run make