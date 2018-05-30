# commaDB (,)

Motivation
----------

I wanted to teach some of my students some of the concepts of databases, but found that there was no intuitive way to see the backing data to them besides passing CSVs into them and then seeing the resulting queries. So I thought that a highly portable database engine that uses the ubiquotous CSV might be just the ticket. Then when I started planning the idea, I started realizing that this is actually more than a teaching aid, but a good way to prototype database systems or to create your own hacker friendly apps since it's easier to directly modify the files that get used in the database when they're just plaintext files in the [RFC4180][01] standard format for comma-separated-values.


What Is It?
-----------

It's just a server written *(and cli application)* that reads and writes to the local filesystem using SQL query languages in the same way anyone would with any other well known SQL database. The difference is, Go parses the SQL and then manages the backing CSV files to create, remove, update, delete **(CRUD)** database tables, records, etc.


References
----------
1. [RFC4180 Specification for CSV Files][01]
2. [ThoughtSpot: 6 Rules for Creating Valid CSV Files][02]

[01]: https://tools.ietf.org/html/rfc4180
[02]: https://www.thoughtspot.com/blog/6-rules-creating-valid-csv-files
