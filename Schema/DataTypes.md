### Data Types convention that is used in WaM-DaM physical data model (database)
=====================
***I borrowed this conversion from ODM1 and ODM2***

No. |Example representative attributes   | Physical data type
----| ------------- | -------------
1   |DateCreated | Date
2   |Description, definition   | VarChar (500)
3   |Name, Link, Type  | VarChar (255)
4   |UserID (Primary keys) | Integer
5   |Code, color, shape | VarChar (50)
6   |DataValue, coordinates, length | Float
7   |IsGeographic? | Bit (5)
8   |DateTimeUTC  | DateTime
