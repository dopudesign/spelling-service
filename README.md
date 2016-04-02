# spelling-service
Please write a simple HTTP web service that provides a RESTful API to determine if a word is misspelled of not. If it is, the API should return some spelling suggestions in a JSON response with a response code.

##Examples of misspelled words
1. Words that have repeating characters (ex. balloooooon)
2. Words that are missing one or more vowels (ex. balln)
3. Words with improper casing (ex. BaLLooN)
4. Any combonation of 1-3
 
## Resouces
1. Dictionary - http://tinyurl.com/bvapsn7
 
## Responses
1. The end point should be `/spelling/:word`
2. Please use `4200` as the default port so the API can be hit using `curl http://localhost:4200/spelling/House`
 
## Service needs to return
1. `404` if the word was not found in the dictionary
2. `200` is the word was found
 
## Examples
**URL:** `http://localhost:4200/spelling/Balloon` <br />
**Response Code:** `200` <br />
**Response Body:** `{correct: true}` <br />

**URL:** `http://localhost:4200/spelling/BallooN` <br />
**Response Code:** `200` <br />
**Response Body:** `{correct: false, suggestions: ["abalone", "balloon"]}` <br />

**URL:** `http://localhost:4200/spelling/fluffyfucknonsense` <br />
**Response Code:** `404` <br />

**URL:** `http://localhost:4200/spelling/dua` <br />
**Response Code:** `404` <br />

## Requirements
1. Use whatever language you want
2. You can use any open source libraries you'd like to **but not library can be used to handle the core algorithmic work for this exercise (spell checking)
3. Add on to the end of this README.md file to document how to use your service.
