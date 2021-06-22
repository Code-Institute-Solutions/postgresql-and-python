# 05 - Running Basic Queries

---

### Create a new file called "sql-expression.py"
- `touch sql-expression.py`

### Query 1 - select all records from the "Artist" table
- `select_query = artist_table.select()`

### Query 2 - select only the "Name" column from the "Artist" table
- `select_query = artist_table.select().with_only_columns([artist_table.c.Name])`

### Query 3 - select only 'Queen' from the "Artist" table
- `select_query = artist_table.select().where(artist_table.c.Name == "Queen")`

### Query 4 - select only by 'ArtistId' #51 from the "Artist" table
- `select_query = artist_table.select().where(artist_table.c.ArtistId == 51)`

### Query 5 - select only the albums with 'ArtistId' #51 on the "Album" table
- `select_query = album_table.select().where(album_table.c.ArtistId == 51)`

### Query 6 - select all tracks where the composer is 'Queen' from the "Track" table
- `select_query = track_table.select().where(track_table.c.Composer == "Queen")`
