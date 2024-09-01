# Analysis-with-SQL: Capstone 2 Project
Database Management System for a Fictional Music Company
## Record Company Database Documentation   
### 1. Database Creation
The database schema for the record company is named record_company. It is created and set to use with the different SQL commands
### 2. Table Structures
#### 2.1 Bands Table
The bands table stores information about the bands. It has two columns: id and name.
#### 2.2 Albums Table
The albums table stores information about albums released by bands. It has four columns: id, name, release_year, and band_id. The band_id column is a foreign key referencing the id column in the bands table
#### 2.3 Songs Table
The songs table stores information about songs in each album. It has four columns: id, name, length, and album_id. The album_id column is a foreign key referencing the id column in the albums table.
### 3. Query
1. Select only the names of all Bands from the songs table
2. Select the oldest album.
3. Get all the bands that have albums
4. Get all the bands that have no albums
5. Get the longest album
6. Insert a record for your favourite Band and one of their Albums
7. Delete the band and album you added to the previous question.
8. Get the Average length of all songs
9. Select the longest song of each album
10. Get the number of songs for each band
11. Create a decade column by dividing the year
12. Filter the Albums which start with the word 'The'
13. Find the album which was released from 2008 to 2013.
