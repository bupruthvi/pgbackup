pgbackup
=========

CLI for backing up remote PostgreSQL databases locally or to AWS s3

Preparing for DEvelopment
--------------------------
1. Ensure ``pip`` and ``pipenv`` are installed.
2. Clone the repository ``git clone git@github.com:example/pgbackup``
3. Fetch development dependencies: ``make install``

Usage
-----

Pass in a full database url, the storage driver and destination.

S3 Example w/ buckate name:

::

        $pgbackup postgres://bob@example.com:54321/db_one --driver s3 backups

Local Example:
::

        $pgbackup postgres://bob@example.com:54321/db_one --driver local /var/local/db_one/backups/dump.sql

Running Test
------------

Run test locally using ``make`` if virtualenv is active:

::

        $ make

if virtualenv isnt active then use:

::

        $ pipenv run make
