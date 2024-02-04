#### List File
```dataview 
LIST file.ctime
```

#### List Rating
##### Rating 1
```dataview 
LIST FROM "1️⃣ Primary Sources" where rating = "1/5"
```
##### Rating 2
```dataview 
LIST FROM "1️⃣ Primary Sources" where rating = "2/5"
```
##### Rating 3
```dataview 
LIST FROM "1️⃣ Primary Sources" where rating = "3/5"
```
##### Rating 4
```dataview 
LIST FROM "1️⃣ Primary Sources" where rating = "4/5"
```
##### Rating 5
```dataview 
LIST FROM "1️⃣ Primary Sources" where rating = "5/5"
```


#### List Activity
```dataview
LIST
FROM "📆 Activity"
```

#### List  One Week
```dataview
LIST
WHERE file.mtime >= date(today) - dur(1 week)
```

#### Logs table
```dataview
TABLE workout
FROM "2️⃣ Collections"
SORT file.ctime DESC
LIMIT 14
```

#### Primary source table
```dataview 
TABLE DOI, Title FROM "1️⃣ Primary Sources" where rating = "5/5"
```

#### Completed Task
```dataview
TASK
WHERE !completed
LIMIT 10
GROUP BY file.link
SORT rows.file.ctime ASC
```

#### Calender

```dataview
CALENDAR file.mtime
FROM ""
```
#### Task

```dataview
TASK
```