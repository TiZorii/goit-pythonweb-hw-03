### Topic 3. Homework

Your goal is to implement the simplest web application. Use the following files from this repository: [https://github.com/GoIT-Python-Web/FullStack-Web-Development-hw3](https://github.com/GoIT-Python-Web/FullStack-Web-Development-hw3).

### Technical Description of the Task

Following the example discussed in the notes, create a web application with routing for two HTML pages: `index.html` and `message.html`.

Additionally:

- Handle static resources such as `style.css` and `logo.png` during the application’s operation.
- Organize form handling on the `message.html` page.
- In case of a 404 Not Found error, return the `error.html` page.
- Your application should run on port 3000.

When working with the form, convert the received byte string into a dictionary and store it in the `data.json` file inside the `storage` directory.

The format of the `data.json` file should be as follows:

```json
{
  "2022-10-29 20:20:58.020261": {
    "username": "krabaton",
    "message": "First message"
  },
  "2022-10-29 20:21:11.812177": {
    "username": "Krabat",
    "message": "Second message"
  }
}
```
Where the key of each message is the timestamp when the message was received (`datetime.now()`). This means that each new message from the web application is appended to the `storage/data.json` file with the timestamp of when it was received.

Add a `/read` route. When this route is accessed, it should generate an informational page. This page must be a Jinja2 template and should display all saved messages from the `data.json` file.

### Additional Task
This is an optional task and is not required for submission of this homework.

- Create a `Dockerfile` and run your application as a Docker container.
- Use the `volumes` mechanism to store data from `storage/data.json` outside the container.

