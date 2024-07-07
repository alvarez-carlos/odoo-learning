#crear un folder para guardar la instancia de odoo
mkdir C:/Users/carlos.alvarez/odoo-dev/projectname


# accede a al folder creado 
cd C:/Users/carlos.alvarez/odoo-dev/projectname


# crea un entorno virtual de python en un subdirectorio llamado env
python -m venv env

# creamos los subdirectorios necesarios
mkdir src local bin filestore logs


# configuracion de odoo. Clonamos odoo, la version 17 de odoo
git clone -b 17.0 --single-branch --depth 1 https://github.com/odoo/odoo.git src/odoo


# instalamos los requisitos
./env/Scripts/pip install -r ./src/odoo/requirements.txt

# configuracion de odoo.bat. Creamos un archivo odoo.bat dentro del folder bin y colocamos dentro del archivo odoo.bat el siguiente codigo:
@echo off
setlocal
set ROOT=%~dp0..
set PYTHON=%ROOT%/env/Scripts/python.exe
set ODOO=%ROOT%/src/odoo/odoo-bin
%PYTHON% %ODOO% -c "%ROOT%/odoo17win.cfg" %*
endlocal
exit /b %errorlevel%


# Configuración adicional. Crear un modulo local vacio. 
mkdir ./local/dummy
touch local/dummy/__init__.py
echo '{"name": "dummy", "installable": False}' > ./local/dummy/__manifest__.py

# Generar archivo de configuracion y configurar git. Ejecutamos odoo.bat con los parametros necesarios:
./bin/odoo.bat --stop-after-init --save --addons-path="C:/Users/carlos.alvarez/odoo-dev/odoo17/src/odoo/addons","C:/Users/carlos.alvarez/odoo-dev/odoo17/local" --data-dir="C:/Users/carlos.alvarez/odoo-dev/odoo17/filestore"

# ==> resultado del comando anterior: 
$ ./bin/odoo.bat --stop-after-init --save --addons-path="C:/Users/carlos.alvarez/Pictures/odoo-dev/odoo17win/src/odoo/addons","C:/Users/carlos.alvarez/Pictures/odoo-dev/odoo17win/local" --data-dir="C:/Users/carlos.alvarez/Pictures/odoo-dev/odoo17win/filestore"
filestore";1c1287f3-7835-46c7-8ef4-e9080bc79b7d2024-06-16 22:04:22,043 3452 INFO ? odoo: Odoo version 17.0 
2024-06-16 22:04:22,044 3452 INFO ? odoo: Using configuration file at C:\Users\carlos.alvarez\Pictures\odoo-dev\odoo17win\odoo17win.cfg

2024-06-16 22:04:22,044 3452 INFO ? odoo: addons paths: ['C:\\Users\\carlos.alvarez\\Pictures\\odoo-dev\\odoo17win\\src\\odoo\\odoo\\addons', 'c:\\users\\carlos.alvarez\\pictures\\odoo-dev\\odoo17win\\filestore\\addons\\17.0', 'c:\\users\\carlos.alvarez\\pictures\\odoo-dev\\odoo17win\\src\\odoo\\addons', 'c:\\users\\carlos.alvarez\\pictures\\odoo-dev\\odoo17win\\local', 'c:\\users\\carlos.alvarez\\pictures\\odoo-dev\\odoo17win\\src\\odoo\\odoo\\addons']
2024-06-16 22:04:22,044 3452 INFO ? odoo: database: default@default:default
2024-06-16 22:04:22,585 3452 INFO ? odoo.addons.base.models.ir_actions_report: You need Wkhtmltopdf to print a pdf version of the reports.
2024-06-16 22:04:24,028 3452 INFO ? odoo.service.server: Initiating shutdown 
2024-06-16 22:04:24,028 3452 INFO ? odoo.service.server: Hit CTRL-C again or send a second signal to force the shutdown.


# creamos un archivo .gitignore en el directorio raiz del proyecto
# Ignorar archivos de configuración específicos
/env/
/src/
/filestore/
/logs/

# Ignorar archivos compilados de Python
*.pyc

# Ignorar archivos de respaldo de Emacs
*~

# Ignorar cualquier archivo oculto por defecto
.*/



# Inicializar un repositorio Git:
git init
git add .
git commit -m "Initial version of odoo17win"


# start odoo
# initiate the environment
venv/Scripate/activate

#initiate odoo server
./bin/odoo.bat -c ./odoo17win.cfg