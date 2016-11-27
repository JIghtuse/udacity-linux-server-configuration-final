# udacity-linux-server-configuration-final
Final project for Udacity Linux Server Configuration course

## Server details

IP address: 35.160.212.183
URL of 'Book catalog' project: http://35.160.212.183/
URL of 'Portfolio' project: http://35.160.212.183/portfolio/

## Summary

### Software installed

Following packets was installed on the server:

* apache2
* libapache2-mod-wsgi-py3
* postgresql-9.3
* git
* postgresql-server-dev-9.3
* python3-pip

Book catalog dependencies installed to virtualenv:

        click==6.6
        Flask==0.11.1
        itsdangerous==0.24
        Jinja2==2.8
        MarkupSafe==0.23
        psycopg2==2.6.2
        requests==2.12.1
        SQLAlchemy==1.1.4
        Werkzeug==0.11.11

### Configuration made

* Created `grader` user
* `grader` added to sudoers file
* Installed packages was updated
* Default SSH port was changed to 2200
* Configured UFW to allow only SSH, HTTP, and NTP ports
* Timezone was set to UTC
* Created apache `site` configuration for projects (/etc/apache2/sites-available/UdacityProjects.conf)
* Forbid accessing .git directories in Apache config file
* Enabled proxy on Apache for Flask (port 5000, file /etc/apache2/sites-available/000-default.conf)
* Configured PostgreSQL for Book project (user and database created, remote connections forbidden)
* Book project software installed (/var/www/catalog) and its API keys configured for server
* Portfolio project installed (/var/www/portfolio)


### Resources used:

* http://docs.sqlalchemy.org/en/latest/
* https://www.postgresql.org/docs/
* http://stackoverflow.com/a/25358092
* http://stackoverflow.com/a/17916515
