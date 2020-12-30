# XHR-GET-Requests-IV
1. In the previous exercise, you made a GET request to the Datamuse API to find words that rhyme. In this exercise, we will create a request to set a topic and find adjectives that describe the input word using query strings.  A query string contains additional information to be sent with a request. The Datamuse API allows us to retrieve more specific data with query strings attached to the request URL.  Wiki: query string A query string is separated from the URL using a ? character. After ?, you can then create a parameter which is a key value pair joined by a =. Examine the example below:  'https://api.datamuse.com/words?key=value' If you want to add an additional parameter you will have to use the &amp; character to separate your parameters. Like so:  'https://api.datamuse.com/words?key=value&amp;anotherKey=anotherValue' Let’s incorporate this into our code!



**### QQQQQQQQQQQQQQQQQQQQQQQQQQQQQQQQQQQQQQ**

1.
Let’s do something else besides finding words that rhyme. Have const queryParams store the value 'rel_jjb='. This will search for words that describe another word.

Run the code. Then, type in a word and click the submit button on the web page.

Checkpoint 2 Passed

Hint
You’ll find queryParams near the top of main.js. Assign it 'rel_jjb='

const queryParams = 'rel_jjb='
2.
Since we want to retrieve more specific results, we should create another parameter. Create another const additionalParams underneath queryParams, and assign it '&topics='.

Reminder: the & character at the start of the string is used to separate our parameters. The = character will join the key 'topics' to a value.

Checkpoint 3 Passed

Hint
Hint: The syntax will look like:

const someVar = 'assigned string'
3.
Now, if you were wondering why there’s a second input field, that’s exactly what we’re going to hook up now! The word typed in here will be the value portion of our second parameter.

The second parameter will filter the response using the word typed into the second input field. In the next step, we’ll incorporate this parameter in with our query string.

In the code block of getSuggestions(), under wordQuery, declare a const topicQuery, and assign it to the value of topicField.

Checkpoint 4 Passed

Hint
To access the value of topicField use dot notation like so:

const topicQuery = topicField.value
4.
In getSuggestions(), change the value of endpoint to a concatenated string of url, queryParams, wordQuery, additionalParams, and topicQuery.

Run the code. Then enter a word and a topic and click submit.

Our request will have returned a response of adjectives that are related to a topic! Feel free to play around with variables and parameters to get more word suggestions!

Checkpoint 5 Passed

Hint
To concatenate a string you have a few options, here’s the syntax for two techniques below:

const word1 = ‘hello’;
const word2 = ‘world!’;
 
console.log(word1 + ' ' + word2);
// ‘hello world!’
You can also interpolate it using a template literal, but remember to use backticks!

console.log(`${word1} ${word2}`);
// ‘hello world!’
