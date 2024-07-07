--- Postgre installation
-- PostgreSQL v16.3-2 - PGSQL15 -  Default port: 5432
https://www.enterprisedb.com/postgresql-tutorial-resources-training-2?uuid=d732dc13-c15a-484b-b783-307823940a11&campaignId=Product_Trial_PostgreSQL_16
-PostgreSQL
-pgAdmin4
-Command Line Tools
-Stack Builder
  - Add-ons, tools and utilities
    -pgAgent 64 bit v4.2.2-1
      pgAgent is a job scheduling agent for PostgreSQL, capable of running multi-step batch/shell and SQL tasks on complex schedules. pgAgent can be managed using pgAdmin.
    -EDB Language Pack v4.3-1
      The Language Pack installer contains the required versions of Python, Perl and TCL/TK for use with pl/python, pl/perl and pl/tcl in PostgreSQL and EPAS
    -pgBouncer v1.22.1-1  Port: 6432
      pgBouncer is a lightweight connection pooler for PostgreSQL.      
  -Database Drivers
    -Npgsql v3.2.6-3
      A .NET data provider for PostgreSQL.  Packaged by EnterpriseDB.
    -pgJDBC
     A collection of JDBC drivers for PostgreSQL (JDBC3, JDBC4 and JDBC41). Packaged by EnterpriseDB. Source code download: http://www.enterprisedb.com/products/download.do
    -psqlODBC
      The official PostgreSQL ODBC driver (64bit version). Packaged by EnterpriseDB.
  -Database Server
    -PostgreSQL 64bit v16.3-2
  -Spatial Extensions
    -PostGIS 2.3 Bundle for PostgreSQL 16 (64bits) v3.4.2
      PostGIS 3.4.2 bundle includes PostGIS 3.4.2 w GDAL 3.8.5 (SQLite 3.30.1, OpenJPEG 2.4.0, Expat 2.4.8, FreeXL 1.0.6, Arrow 13.0.0)  , GEOS 3.12.1, Proj 8.2.1, pgRouting 3.6.2,  osm2pgrouting 2.3.8, ogr_fdw 1.1.4 spatial foreign data wrapper extension, and pgPointcloud 1.2.4, h3-pg 4.1.3, MobilityDb 1.1.1.

      https://postgis.net/2024/02/PostGIS-Patch-Releases/

      PostGIS "spatially enables" the PostgreSQL server, allowing it to be used as a backend spatial database for geographic information systems (GIS). PostGIS follows the OpenGIS "Simple Features Specification for SQL" and has been certified as compliant with the "Types and Functions" profile. 

      https://github.com/pgRouting/pgrouting/releases/tag/v3.6.2
      pgRouting extensions PostGIS for building routing applications

      https://github.com/pgRouting/osm2pgrouting
      osm2pgRouting for loading OSM data into pgrouting

      https://github.com/pramsey/pgsql-ogr-fdw
      ogr_fdw allows you to query flat files, relational databases, and web services to name a few.  Spatial columns get transformed to PostGIS geometry columns.

      https://github.com/pgpointcloud/pointcloud
      pgPointcloud introduces specialty types for storing point cloud data loaded from LIDAR.

      https://github.com/zachasme/h3-pg
      Uber h3 api with conversion of h3 index to postgis geometries.

      https://github.com/MobilityDB/MobilityDB
      MobilityDb for managing spatial trajectories
  -Web Development
    -PEM-HTTPD v2.4.58-2   C:\Program Files\edb\pem\httpd    Port: 8081
      PEM-HTTPD is a preconfigured Apache webserver, compiled for use with PostgreSQL. Packaged by EnterpriseDB.

      Source code download: http://www.enterprisedb.com/products/download.do
  -Registration Required and Trial Products
    -EnterpriseDB Tools
      -Migration Toolkit
      -PEM SQL Profiler Plugin for PostgreSQL
      -Postgres Entreprise Manager Agent
      -Postgres Entreprise Manager Server
      -Replication Server
      -SQL/Potect for PostgreSQL

-- postgres conf file
C:\Program Files\PostgreSQL\16\data\pg_hba.conf
