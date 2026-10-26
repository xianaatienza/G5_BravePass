# G5_BravePass
BraveHeart Pass (BravePass): Campus Parking Car Pass System

BravePass is a campus parking system with two parts: a web page for guards and ATC staff, and an API that stores car passes in SQL Server.

Guards check a plate number and see who owns the car and what type it is.
ATC staff add, edit, remove, upload (CSV) and export car passes.
The database is SQL Server. You can view the data in SSMS.

Features

Front end

Parking lot grid with Students, Faculty and Guests zones (tap a slot to occupy or free it; the lot status resets on refresh)
Verify plate number: shows owner and car type, or "No car pass on file"
Plates match ignoring spaces, dashes and case ("abc 1234" = "ABC-1234")
ATC section (hidden behind a password): add or update a pass, search, remove, delete all
CSV upload, CSV template and CSV export
Light and dark mode, works on phones

API

GET, POST, PUT, PATCH and DELETE for car passes
Duplicate plates are rejected (unique index on the normalized plate)
Database and table are created automatically on first run
Swagger page for testing at /swagger
