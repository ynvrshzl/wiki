```dataview
table without id
file.link as "Files",
dateformat(file.ctime, "h:mm a") as "Created"
where file.cday = date(today)
sort file.ctime desc
```