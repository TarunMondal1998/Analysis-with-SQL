# Analysis-with-SQL
Database Management System for a Fictional Music Company
<h1>Record Company Database Documentation</h1>
    
    <h2>1. Database Creation</h2>
    <p>The database schema for the record company is named <strong>record_company</strong>. It is created and set to use with the following SQL commands:</p>
    <pre><code>CREATE SCHEMA record_company;
USE record_company;
</code></pre>

    <h2>2. Table Structures</h2>

    <h3>2.1 Bands Table</h3>
    <p>The <strong>bands</strong> table stores information about the bands. It has two columns: <code>id</code> and <code>name</code>.</p>
    <pre><code>CREATE TABLE bands (
  id INT NOT NULL AUTO_INCREMENT,
  name VARCHAR(255) NOT NULL,
  PRIMARY KEY (id)
);
</code></pre>

    <h3>2.2 Albums Table</h3>
    <p>The <strong>albums</strong> table stores information about albums released by bands. It has four columns: <code>id</code>, <code>name</code>, <code>release_year</code>, and <code>band_id</code>. The <code>band_id</code> column is a foreign key referencing the <code>id</code> column in the <strong>bands</strong> table.</p>
    <pre><code>CREATE TABLE albums (
  id INT NOT NULL AUTO_INCREMENT,
  name VARCHAR(255) NOT NULL,
  release_year INT,
  band_id INT NOT NULL,
  PRIMARY KEY (id),
  FOREIGN KEY (band_id) REFERENCES bands(id)
);
</code></pre>

    <h3>2.3 Songs Table</h3>
    <p>The <strong>songs</strong> table stores information about songs in each album. It has four columns: <code>id</code>, <code>name</code>, <code>length</code>, and <code>album_id</code>. The <code>album_id</code> column is a foreign key referencing the <code>id</code> column in the <strong>albums</strong> table.</p>
    <pre><code>CREATE TABLE songs (
  id INT NOT NULL AUTO_INCREMENT,
  name VARCHAR(255) NOT NULL,
  length FLOAT NOT NULL,
  album_id INT NOT NULL,
  PRIMARY KEY (id),
  FOREIGN KEY (album_id) REFERENCES albums(id)
);
</code></pre>

    <h2>3. Data Insertion</h2>
    
    <h3>3.1 Inserting Data into Bands Table</h3>
    <p>Data for the <strong>bands</strong> table is inserted using the following SQL commands:</p>
    <pre><code>INSERT INTO bands(id,name) VALUES (1,'Seventh Wonder');
INSERT INTO bands(id,name) VALUES (2,'Metallica');
INSERT INTO bands(id,name) VALUES (3,'The Ocean');
INSERT INTO bands(id,name) VALUES (4,'Within Temptation');
INSERT INTO bands(id,name) VALUES (5,'Death');
INSERT INTO bands(id,name) VALUES (6,'Van Canto');
INSERT INTO bands(id,name) VALUES (7,'Dream Theater');
</code></pre>

    <h3>3.2 Inserting Data into Albums Table</h3>
    <p>Data for the <strong>albums</strong> table is inserted using the following SQL commands:</p>
    <pre><code>INSERT INTO albums(id, name, release_year, band_id) VALUES (1, 'Tiara', 2018, 1);
INSERT INTO albums(id, name, release_year, band_id) VALUES (2, 'The Great Escape', 2010, 1);
...
INSERT INTO albums(id, name, release_year, band_id) VALUES (18, 'Tribe of Force', 2010, 6);
</code></pre>

    <h3>3.3 Inserting Data into Songs Table</h3>
    <p>Data for the <strong>songs</strong> table is inserted using the following SQL commands:</p>
    <pre><code>INSERT INTO songs(id,name,length,album_id) VALUES (1,'Arrival',1+(30/60),1);
INSERT INTO songs(id,name,length,album_id) VALUES (2,'The Everones',6+(13/60),1);
...
INSERT INTO songs(id,name,length,album_id) VALUES (91,'Master of Puppets',8+(35/60),4);
</code></pre>

    <h2>4. Summary</h2>
    <p>This documentation provides an overview of the database schema for a record company, detailing the creation of the schema, table structures, and data insertion scripts. This schema helps in organizing the data related to bands, albums, and songs efficiently.</p>

