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

---

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

---

### Show students whose majors are not related to the data!
```
SELECT first_name, major
FROM students
WHERE
major NOT LIKE 'Data%' and major != 'null'
```

<strong> Result : </strong>

![image](https://user-images.githubusercontent.com/112471006/200634068-f1a5f068-5b1e-4da7-9bb3-266e667ad992.png)

---

### Displays and lists the majors in a course!
```
SELECT course,
COUNT (DISTINCT major) AS total_major,
STRING_AGG(DISTINCT major, ', ') AS list_of_major
FROM courses
GROUP BY courses.course
```

<strong> Result : </strong>

![image](https://user-images.githubusercontent.com/112471006/200896965-d0989d9a-ea72-4043-b9c9-34e79c389247.png)

---

### Show the order of the majors that students follow the most and a list of names of participants who follow it!
```
SELECT major,
COUNT (first_name) AS total_students,
STRING_AGG(first_name, ', ') AS list_of_students
FROM students
WHERE major != 'null'
group by major
ORDER BY total_students DESC
```

<strong> Result : </strong>

![image](https://user-images.githubusercontent.com/112471006/200900189-d453f447-7738-484a-be35-24d8a4aacc04.png)

---




