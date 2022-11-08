# Processing databases about students and their majors.

### Show the name of the student whose major is the database administration!
```
SELECT first_name, major
FROM students
WHERE 
major = 'Database Administration'

```
<strong> Result : </strong>

![image](https://user-images.githubusercontent.com/112471006/200624676-291c549e-7e68-497a-9dd4-c11fd1c6552e.png)

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

![image](https://user-images.githubusercontent.com/112471006/200626998-a91f1eda-6194-469f-8d2b-6ac2988349ef.png)
