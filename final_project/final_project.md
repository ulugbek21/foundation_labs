# Final project

Create a bookstore REST API where customers rent books. The backend will have information about **customers** and **books**.

It also stores **rental information** to keep track of who rents which book and when.

1. CRUD APIs for **customers**.
```
customer: {
    id: int,
    firstname: string,
    lastname: string,
    email: string,
    phone: string,
    date_of_birth: string,
    address: string,
    created_at: datetime,
    updated_at: datetime
}
```
Example:
```json
{
  "id": 1,
  "firstname": "John",
  "lastname": "Doe",
  "email": "john.doe@example.com",
  "phone": "+998987654321",
  "date_of_birth": "20-04-1998",
  "address": "221B Baker Street, London",
  "created_at": "2022-03-26T09:08:44.000000Z",
  "updated_at": "2022-03-26T09:08:44.000000Z"
}
```

2. CRUD APIs for **books**.
```
book: {
    id: int,
    isbn: string,
    title: string,
    gender: string,
    description: string,
    author: string,
    publish_year: int,
    cover_photo_url: string,
    created_at: datetime,
    updated_at: datetime
}
```
Example:
```json
{
  "id": 1,
  "isbn": "978-0393058000",
  "title": "Sherlock Holmes",
  "gender": "fictional detective",
  "description": "Sherlock Holmes (/ˈʃɜːrlɒk ˈhoʊmz/) is a fictional detective created by British author Sir Arthur Conan Doyle. Referring to himself as a consulting detective in the stories, Holmes is known for his proficiency with observation, deduction, forensic science and logical reasoning that borders on the fantastic, which he employs when investigating cases for a wide variety of clients, including Scotland Yard.",
  "author": "Arthur Conan Doyle",
  "publish_year": 2006,
  "cover_photo_url": "https://images-na.ssl-images-amazon.com/images/I/91hJe52QzjL.jpg",
  "created_at": "2022-03-26T09:08:44.000000Z"
}
```
3. Create and Update APIs for **rental_infos**.
```
rental_info: {
    customer_id: int,
    book_id: int,
    booked_day: date,
    returned_day: date,
    created_at: datetime,
    updated_at: datetime
}
```
Example:
```json
{
  "customer_id": 1,
  "book_id": 1,
  "booked_day": "2022-05-22",
  "returned_day": "2022-09-26",
  "created_at": "2022-03-26T09:08:44.000000Z",
  "updated_at": "2022-03-26T09:08:44.000000Z"
}
```
4. Search API to retrieve customer list **by name**(firstname and lastname).
5. Search API to retrieve book list **by title**.
6. (Optional) Get API to retrieve given customer **rental infos**.
7. (Optional) Save results in file.
8. (Optional) Organize project layout in folders.