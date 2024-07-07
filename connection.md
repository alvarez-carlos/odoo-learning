name: PGSQL15
hostname: localhost
port: 5432
Maintenance database: postgres
username: postgres
password: ******
-------------
sstep 1:
C:\Users\carlos.alvarez\Pictures\odoo17\server\odoo.conf
create postgresql credentials for in the odoo.conf file:
  ata_dir = C:\Users\carlos.alvarez\Pictures\odoo17\sessions
  db_host = localhost
  db_maxconn = 64
  db_maxconn_gevent = False
  db_name = False
  db_password = openpgpwd
  db_port = 5432
  db_sslmode = prefer
  db_template = template0
  db_user = openpg
  dbfilter = 
  default_productivity_apps = True
  demo = {}
-------------
Use the odoo credentials to create a the db and start odoo server
  Odoo database manager password: *******
  DB: Dev
  Email: ********************
  password: **********
------------
odoo in a virtual environment
Odoo database master password: **********