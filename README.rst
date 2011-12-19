'''What is this?'''
So, Django DB Connection pooling is nonexsistant, and basicly cannot be done because it would need a persistant process for the connection. But, some Searches away there are some solutions that work to a creatin degree[1].
But this approach has some disadvantages and bugs, most notably some field conversion errors (MySQLdb DateTime becomes Time field...) and some subtle bugs (if you don't have DB port specified...).
But because we needed that connection pooling to work, I dug deeper, bothered people (Thanks again zzzek) and finally came up with a better solution that still uses SQLAlchemy and is therefore limited to pooling DBs that SQLAlchemy supports.
In a nutshell, you'll need SQLAlchemy 0.7.3 or newer and a hacked up database backend like this one. 

[1] - http://menendez.com/blog/mysql-connection-pooling-django-and-sqlalchemy/
