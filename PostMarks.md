
# Post Marks

Admin user can able to upload student marks. This API has simple analytics which will make data more meaningful, once a student mark is getting uploaded the API will calculate totalMarks, percentage and status (Pass or Fail based on threshold ) with raw data which was sent by Teacher (ADMIN).

**URL** : `/v1/reports/post/marks`

**Method** : `POST`

**Auth required** : Yes

**Headers**

```json
{
    "userId" : "userId as student roll number",
    "password" : "password as plain text",
    "role" : "Authority (ADMIN)",
    "Authorization": "Token",
}
```

**Request Body**
```json
{
    "rollNo" : "student roll number",
    "standard" : "standard / class",
    "examType" : "Quarterly / HalfYearly / Annual",
    "marks": {"subject":"marks","subject":"marks"}
}


## Success Response

**Code** : `201 Created`

**Content example**

```data
Record Created.
```

## Error Response

**Condition** : Incase of token expired or wrong token entered.

**Code** : `401 UN AUTHORIZED`

**Content** :

```Data
Invalid Token or Token Expired
```
