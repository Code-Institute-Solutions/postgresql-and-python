# 06 - Introducing Class-Based Models

---

### Create a new file called "sql-orm.py"
- `touch sql-orm.py`

### Query 1 - select all records from the "Artist" table
```python
artists = session.query(Artist)
for artist in artists:
    print(artist.ArtistId, artist.Name, sep=" | ")
```

### Query 2 - select only the "Name" column from the "Artist" table
```python
artists = session.query(Artist)
for artist in artists:
    print(artist.Name)
```

### Query 3 - select only "Queen" from the "Artist" table
```python
artist = session.query(Artist).filter_by(Name="Queen").first()
print(artist.ArtistId, artist.Name, sep=" | ")
```

### Query 4 - select only by "ArtistId" #51 from the "Artist" table
```python
artist = session.query(Artist).filter_by(ArtistId=51).first()
print(artist.ArtistId, artist.Name, sep=" | ")
```

### Query 5 - select only the albums with "ArtistId" #51 on the "Album" table
```python
albums = session.query(Album).filter_by(ArtistId=51)
for album in albums:
    print(album.AlbumId, album.Title, album.ArtistId, sep=" | ")
```

### Query 6 - select all tracks where the composer is "Queen" from the "Track" table
```python
tracks = session.query(Track).filter_by(Composer="Queen")
for track in tracks:
    print(
        track.TrackId,
        track.Name,
        track.AlbumId,
        track.MediaTypeId,
        track.GenreId,
        track.Composer,
        track.Milliseconds,
        track.Bytes,
        track.UnitPrice,
        sep=" | "
    )
```
