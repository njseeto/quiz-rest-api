# quiz-rest-api

Making a simple REST API that will be able to retrieve, update, delete and create quiz questions in the database with this project.

Need to add more here:
- What could be used for testing?


To get this project running you need:
- node
- Insomnia
- MongoDB account
- Add a `.env` file in your root configured with the following information:

```
PORT=PORT_NUMBER
DATABASE_CONNECTION=mongodb://<dbuser>:<dbpassword>@ds163103.mlab.com:63103/quiz-rest-api
```

To start the server: `npm run dev`

POSTS
To add a new question to the MongoDB you can add it via the endpoint `/questions` in the following structure:

```
{
	"description":"What was Maya Angelou's real name?",
	"alternatives": [
		{
			"text": "Marguerite Johnson",
			"isCorrect": true
		},
		{
			"text": "Madeline Joseph"
		},
		{
			"text": "Maybelline Beth"
		},
		{
			"text": "Marisol Clark"
		}
	]
}
```

Note the default for the `isCorrect` flag is `false`.