# Databases

## Relational DB

- Relational: all data is represented in terms of tuples (finite lists), grouped into relations. A database organized in terms of the relational model is a relational database
- Relation is a table
- Table consists of rows and columns, attribute is a column, tuple is a row
- 3NF

## SQL

- SQL is a language - Structured Query Language
- SQL consists of a data definition language, data manipulation language, and data control language.
- The scope of SQL includes data insert, query, update and delete, schema creation and modification, and data access control.
- Although SQL is often described as a declarative language. It also includes procedural elements.
- Various RDBMS vendors provide their implementation of the SQL

## MySQL vs MariaDB

- MySQL is an Open Source handled by Oracle
- MariaDB is a fork of MySQL led by original developers of MySQL
- MySQL Cookbook: [MySQLCookbook](http://shop.oreilly.com/product/0636920032274.do)

## PDO

- The PHP Data Objects (PDO) extension defines a consistent interface for accessing databases in PHP.
- Each database driver that implements the PDO interface can expose database-specific features as regular extension functions
- You must use a database-specific PDO driver to access a database server
- PDO provides a data-access abstraction layer, which means that, regardless of which database you're using, you use the same functions to issue queries and fetch data
- PDO does not provide a database abstraction; it doesn't rewrite SQL or emulate missing features. You should use a full-blown abstraction layer if you need that facility
- PDO classes and their most used methods are:
  - [PDO](http://php.net/manual/en/class.pdo.php)
    - [PDO::query](http://php.net/manual/en/pdo.query.php)
    - [PDO::prepare](http://php.net/manual/en/pdo.prepare.php)
    - [PDO::exec](http://php.net/manual/en/pdo.exec.php)
  - [PDOStatement](http://php.net/manual/en/class.pdostatement.php)
    - [PDOStatement::bindParam](http://php.net/manual/en/pdostatement.bindparam.php)
    - [PDOStatement::bindValue](http://php.net/manual/en/pdostatement.bindvalue.php)
    - [PDOStatement::execute](http://php.net/manual/en/pdostatement.execute.php)
    - [PDOStatement::fetch](http://php.net/manual/en/pdostatement.fetch.php)
    - [PDOStatement::fetchAll](http://php.net/manual/en/pdostatement.fetchall.php)
  - [PDOException](http://php.net/manual/en/class.pdoexception.php)
- Basic usage:
  - Get a connection
  - Prepare a statement and get a PDOStatement instance
  - Optional: Bind values or parameters
  - Execute
  - Fetch data if needed
- About transactions: [Transactions](http://php.net/manual/en/pdo.transactions.php)

## Doctrine DBAL

- The Doctrine database abstraction & access layer (DBAL) offers a runtime layer around a PDO-like API and a lot of additional, horizontal features like database schema introspection and manipulation through an OO API

## Query Builders

- [php-sql-query-builder](https://github.com/nilportugues/php-sql-query-builder)
- [pixie](https://github.com/usmanhalalit/pixie)

## ORM

- Is a programming technique for converting data between incompatible type systems in object-oriented programming languages
- This creates a "virtual object database" that can be used from within the programming language
- ORM patterns: [ORM](http://www.giorgiosironi.com/2009/08/10-orm-patterns-components-of-object.html)
- ActiveRecord and Repository are considered as most popular
- Popular ORMs:
  - Doctrine ORM: [Doctrine](http://docs.doctrine-project.org/projects/doctrine-orm/en/latest/)
  - Eloquent ORM: [Eloquent](https://laravel.com/docs/master/eloquent)
  - Propel ORM: [Propel](http://propelorm.org/)


# Excercise

- Build an RSS/Atom feed reader that reads RSSes from URL(s) provided and stores them in a DB
- You can use specialized libraries to fetch feeds (SimplePie, Guzzle, etc.)
- Run the reader script every 1 (5, 10) minutes to fetch and store data
- Provide a front-client to display the list of news items
- Optional: handle pagination, number of items etc
