# Tech-task-backend
# Tech-Task-Backend

## Task 1
* Implement JWT authentication
```
Request Example
{
  "username": "user123",
  "password": "securepa55w0rd"
}
Response example
{
  "token" : "eddjehjefgjhefhe.fuwigfy3gryfygsf.fjeghejgf4ygfwhegfjhwef',
  "FullName" : "John Doe"
}
```
* Admin can Add user
```
Request example
{
  "username" : "user123",
  "password" : "securepa55w0rd",
  "firstName" : "John",
  "lastName" : "Doe",
  "roles" :
    "manager",
    "teacher"
}
```

### Role Management
* CRUD for roles
* Assign user roles
* Default roles - Admin, Manager

## Task 2

### Create Group - Only for Admin users
```
Request example
{
    "name" : "ZedGroup",
    "mentorId" : 1,   // Foreign key => User
    "price" : 300
}
```
### Update Group - Accessible to Admin users
```
Request example
{
    "id": 1,
    "name" : "ZedGroup",
    "mentorId" : 1,   // Foreign key => User
    "price" : 300
}
```

### Get Group - Accessible to Admin and Teacher
```
Request GET -  groups/{id}
Response Example
{
    group : {
    "id' : 1,
    "Name" : 'ZedGroup",
    "Price": 300
    "Mentor" "John Doe",
    "students":
    [
        {
            "id": 1,
            "fullName" : "Student 1",
            "JoinedAt" : "2025-04-04T11:48:15.568Z",
            // other student details
        },
        {
            "id": 2,
            "fullName" : "Student 2",
            "JoinedAt" : "2025-04-04T11:48:15.568Z",
            // other student details
        }
    ]
}
```
### Get groups list - Accessible to Admin and Teacher
```
Response example
[
  {
    "id" : 1,
    "name" : "Group 1",
    "price" : 250,
    "mentor" : "John Doe"
    "students : 10
  },
  {
    "id" : 1,
    "name" : "Group 1",
    "price" : 250,
    "mentor" : "John Doe"
    "students : 10
  }
]
```
### Create Student
```
Request example
{
  "fullName" : "Mark Town",
  "phoneNumber" : "+998901234567",
  "dateOfBirth" : ""2003-04-04T11:48:15.568Z" (optional)
  "gender" : "Male",
}
```

### Update student

```
Request example
{
  "id" : 2,
  "fullName" : "Mark Town",
  "phoneNumber" : "+998901234567",
  "dateOfBirth" : ""2003-04-04T11:48:15.568Z" (optional)
  "gender" : "Male",
}
```
### Get students list

```
Response example
[
{
  "id" : 1,
  "fullName" : "Mark Town",
  "phoneNumber" : "+998901234567",
  "dateOfBirth" : "2003-04-04T11:48:15.568Z" (optional)
  "gender" : "Male",
}
{
  "id" : 2,
  "fullName" : "Mark Town",
  "phoneNumber" : "+998901234567",
  "dateOfBirth" : "2003-04-04T11:48:15.568Z" (optional)
  "gender" : "Male",
}
]
```

### Get student details

```
Response example
{
  "id" : 1,
  "fullName" : "Mark Town",
  "phoneNumber" : "+998901234567",
  "dateOfBirth" : "2003-04-04T11:48:15.568Z" (optional)
  "gender" : "Male",
  "groups" : [
    {
      "id" : 1,
      "name" : "Group 1",
      "price" : 250,
      "mentor" : "John Doe",
    },
    {
      "id" : 1,
      "name" : "Group 1",
      "price" : 250,
      "mentor" : "John Doe",
    },
  ]
}
```
### Add student to group
```
Request example
{
  "studentId" : 1,
  "groupId": 2
}
```

### Remove student from group
```
Request example
{
  "studentId" : 1,
  "groupId": 2
}
```


        
