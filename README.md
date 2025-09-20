# 📝 Simple Notes API

## **Objective**

Create a basic REST API using **Express.js** to add and view notes. This is a beginner-friendly task to practice routes, middleware, and handling JSON data.

---

## **Requirements**

### 1. Setup

* Initialize Node.js project with `npm init -y`
* Install Express: `npm install express`
* Create `index.js` for your server
* Server should run on **port 3000**
* Use `express.json()` middleware for parsing JSON

---

### 2. Data Storage

* Keep notes in memory using an array:

```js
let notes = [];
```

---

### 3. API Endpoints

| Method | Endpoint | Description    | Request Body (JSON)                         |
| ------ | -------- | -------------- | ------------------------------------------- |
| GET    | /notes   | Get all notes  | -                                           |
| POST   | /notes   | Add a new note | { "title": "Note 1", "content": "My note" } |

---

### 4. Middleware

* Create a simple logger middleware to print request method and URL:

```js
app.use((req, res, next) => {
  console.log(`${req.method} ${req.url}`);
  next();
});
```

---

## **Bonus (Optional)**

* Assign a unique `id` to each note
* Test your API using **Postman**
* Try adding error handling for missing fields

---

## **How to Run**

1. Open terminal in project folder
2. Run the server:

```bash
node index.js
```

3. Test endpoints:

   * `GET http://localhost:3000/notes`
   * `POST http://localhost:3000/notes` with JSON body:

```json
{ "title": "My Note", "content": "This is a sample note" }
```
