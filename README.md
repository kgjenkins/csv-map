# csv-map

A simple, searchable point map powered by a CSV file.

The CSV file should contain two columns (`longitude` and `latitude`) that contain the point coordinates.

Any other columns can be used for searching or display.


## Example CSV

Each point is represented by a row in the CSV, for example:

| id | longitude | latitude | name | category | description |
| - | - | - | - | - | - |
| 1 | -76.475923 | 42.448822 | Mann Library | library | everyone's favorite place to study |
| 2 | -76.484671 | 42.447781 | Olin Library | library | so many books! |
| 3 | -76.484351 | 42.446664 | The Cornell Store | store | get your books and sweatshirts here |
| 4 | -76.476525 | 42.448659 | Manndible Cafe | restaurant | soup and burritos and chips, located right outside the library |


# Searching

By default, all columns are full-text searchable.

- a search for `mann` will find items 1 and 4 (partial match on "Manndible")
- a search for `library` will find items 1, 2, and 4


# Future plans

In a future version, fielded searches will be allowed:

- a search for `name:library` will find items 1 and 2, but not 4

It will also be possible to specify which fields are searchable, and which are displayed.
