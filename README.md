# Processing databases about students and their majors.

### Show the name of the student whose major is the database administration!
```
SELECT first_name, major
FROM students
WHERE 
major = 'Database Administration'

```
<strong> Result : </strong>

![image](https://user-images.githubusercontent.com/112471006/200629200-f1b4ccc5-bf12-4d32-aa68-d2e008bba1b3.png)

### Show 5 students with the highest GPA and their majors!
```
SELECT first_name,major,gpa
FROM students
WHERE
gpa != 'null'
ORDER BY gpa DESC
Limit 5 

```

<strong> Result : </strong>

![image](https://user-images.githubusercontent.com/112471006/200629257-90f51494-a788-4c24-8a7f-597f8420f8fa.png)
