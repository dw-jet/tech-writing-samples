# Retrieve Results of a Dice Roll
Rolls 10-sided dice against a difficulty and returns the results.

# URL

GET http://localhost:4567/api/v1/roll

# Query Parameters
| Parameter  | Description                                       | Type | Required | Notes              |
|------------|---------------------------------------------------|------|----------|--------------------|
| num_dice   | Number of 10-sided dice to roll.                  | int  | Required |                    |
| difficulty | The number each die must meet or beat to succeed. | int  | Optional | Default value is 6 |
                                                          
# Sample Request

GET http://localhost:4567/api/v1/roll?numDice=4&difficulty=7

# Response

| Element          | Description                                                | Type             | Notes                                                   |
|------------------|------------------------------------------------------------|------------------|---------------------------------------------------------|
| difficulty       | The number the API compared dice to for success. | number           | Between 2 and 10                                        |
| num_dice         | How many dice the API rolled.                                 | number           |                                                         |
| faces            | The result of rolling the dice. One die for each num_dice.           | array of numbers | Dice are 10-sided                                    |
| rolled_successes | The number of dice that met or beat the difficulty          | number           |                                                         |
| rolled_ones      | How many 1s are in the result.              | number           |                                                         |
| total_successes  | The rolled successes minus the rolled ones.                | number           |                                                         |
| outcome          | The overall outcome of the roll.                           | string           | Valid values: "__success__", "__failure__", "__botch__" |
  

# Sample Response
```JSON
{
  "difficulty":5,
  "num_dice":4,
  "faces":[8,9,8,1],
  "rolled_successes":3,
  "rolled_ones":1,
  "total_successes":2,
  "outcome": "success"
}
```

# Status Codes and Errors
The following table lists the returned HTTP status codes.

| Code | Description | Notes                        |
|------|-------------|------------------------------|
| 200  | OK          |                              |
| 400  | Bad Request | A query parameter is invalid |