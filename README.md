# futureproof_documentation


## HouseStuff

### Retrieve array of all house objects
```
GET /houses
{
    data: [
        {}
    ]
}
```

### Retrieve a single house object
```
GET /houses/:id
{
    owner: {
           id
       name
            Age
    }
     house_num
     address_line_1
     address_line_2
         county
         post_code
         
         Residents: [
        {
           id
           name
           age
        },
        {
           id
           name
           age
        }
    ]
    
}
```
### Retrieve address for single house
```
GET /houses/:id/address
    {
       house_num
       address_line_1
       address_line_2
            county
            post_code
    }
```

### Retrieve owner for single house

```
GET /houses/:id/owner
    owner: {
           id
       name
            Age
    }
```

### Retrieve all people
```
GET /people
{
    data: [
        {}
    ]
}
```
### Retrieve single person
```
GET /people/:id
{
    id
    name
         Age
    house: {
           House details...
      numberOfPeople
    }
}
```

### Retrieve people in certain age bracket
```
GET /people/ages/:ageBracket
```
### Retrieve all people that suit household size
```
GET /people/householdsize/:num
```
### Set up a person record
```
POST /people
PUT /people/:id
```
Creates a record for a single person, or update that person's record
```
//delete a person, also removes links in address
DELETE /people/:id
Set up a house
POST /houses
PUT /houses/:id
//delete a house, also removes links in address
DELETE /houses/:id
Creates a record linking person and house
POST /address
```
