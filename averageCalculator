const express = require('express');
const bodyParser = require('body-parser');


const app = express();
const port = 3000;


app.use(bodyParser.json());


app.post('/average', (req, res) => {
  const numbers = req.body.numbers;
  
  if (!Array.isArray(numbers)) {
    return res.status(400).send('Invalid input');
  }

  let sum = 0;
  for (let i = 0; i < numbers.length; i++) {
    sum += numbers[i];
  }
  const average = sum

  res.send({ average: average });
});

app.listen(port, () => {
  console.log(`Server is running on port ${port}`);
});
