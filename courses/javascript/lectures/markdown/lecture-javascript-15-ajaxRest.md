### 15. JavaScript
#### AJAX & REST


---

#### Asynchronous JavaScript and XML

* Is a collection of client based techniques to fetch web based data asynchronos.
* A browser built-in XMLHttpRequest object (to request data from a web server).
* JavaScript and HTML DOM (to display or use the data).
* AJAX applications might use XML to transport data, but it is equally common to transport data as plain text or JSON text.


---

#### With Ajax you can:

* Read data from a web server - after the page has loaded.
* Request data from a server and load it without having to refresh the entire page.
* Update a web page without reloading the page.
* Send data to a web server - in the background.


---

#### Synchronous & Asynchronos

* Execute something <b>synchronously</b> = you wait for it to finish before moving on to another task.
* Standing in line waiting for food
* Execute something <b>Asynchronously</b> = you can move on to another task before it finishes.
* Make an order, sit at the table and wait for your food



---

#### AJAX examples

* Live search - You enter something into a input and you get alternatives matching.
* Tradera - Auctions and bids are updated continually.
* Login without reload.



---

#### How AJAX works

1. The browser request data from the server.
1. The server responds with data (usally HTML, XML, JSON formats).
1. The browser processes the content and adds it to the page.


---

#### AJAX flow
<img width="600" src="/media/javascript-images/javascript-15/ajaxflow.png" alt="AJAX flow">


---
				
#### Data formats

* When exchanging data between a browser and a server, the data can only be text.
* Servers typically send back:
  * <b>HTML</b> - Hyper Text Markup Language.
  * <b>XML</b> - Extensible Markup Language.
  * <b>JSON</b> - JavaScript Object Notation.
	



---

#### XML (Extensible Markup Language)
* XML was designed to store and transport data.
* XML was designed to be both human- and machine-readable.
* XML is more strict than HTML.
* XML tags names describe the data that they contain.

```XML
<note>
	<to>Tove</to>
	<from>Jani</from>
	<heading>Reminder</heading>
</note>
```



---

#### JSON (JavaScript Object Notation)

* JSON is a syntax for storing and exchanging data.
* JSON is text, written with JavaScript object notation.
* JSON is text, and we can convert JavaScript object into JSON, and send JSON to the server.
* Like JavaScript objects JSON objects use key - value pairs.

```JSON
{"menu": {
	"id": "file",
	"value": "File",
	"popup": {
		"menuitem": [
			{"value": "New", "onclick": "CreateNewDoc()"},
			{"value": "Open", "onclick": "OpenDoc()"},
			{"value": "Close", "onclick": "CloseDoc()"}
		]
	}
}}
```


---

#### Working with JSON

* ```JSON.stringify()``` converts JavaScript objects into a string formatted using JSON.
* ```JSON.parse()``` processes a string containing JSON data, converting JSON data into a JavaScript object.

```JSON
{"menu": {
	"id": "file",
	"value": "File",
	"popup": {
		"menuitem": [
			{"value": "New", "onclick": "CreateNewDoc()"},
			{"value": "Open", "onclick": "OpenDoc()"},
			{"value": "Close", "onclick": "CloseDoc()"}
		]
	}
}}
```
```JavaScript
JSON.stringify(object); // Converts to JSON

JSON.parse(response); // Converts JSON response to a JS object
```


---

XML
```XML
<menu id="file" value="File">
	<popup>
		<menuitem value="New" onclick="CreateNewDoc()" />
		<menuitem value="Open" onclick="OpenDoc()" />
		<menuitem value="Close" onclick="CloseDoc()" />
	</popup>
</menu>
```

JSON
```JSON
{"menu": {
	"id": "file",
	"value": "File",
	"popup": {
		"menuitem": [
			{"value": "New", "onclick": "CreateNewDoc()"},
			{"value": "Open", "onclick": "OpenDoc()"},
			{"value": "Close", "onclick": "CloseDoc()"}
		]
	}
}}
```


---

### API
#### Application Programming Interface


---
				

#### What is an API (Application Programming Interface)?

* User interfaces allow humans to interact with programs.
* API's let programs and scripts to talk to each other.


---

#### API real world example
Think of an API like a menu in a restaurant. The menu provides a list of dishes you can order, along with a description of each dish. When you specify what menu items you want, the restaurant’s kitchen does the work and provides you with some finished dishes. You don’t know exactly how the restaurant prepares that food, and you don’t really need to. - <a href="https://www.howtogeek.com/343877/what-is-an-api/">Chris Hoffman</a>


---

#### If I write a script or create some software, websites or web other services, I can decide to open up some of that functionality for others.


---

#### Different types of APIs

* Internal computer API (files, camera etc.).
* Browser API (storage, history, location etc.).
* External RESTful API(Getting and sending data remote).
* SOAP etc.



---

#### Different types of APIs
<img width="800" src="/media/javascript-images/javascript-15/api1.png" alt="apis">


---

#### Different types of APIs
<img style="height: 500px" src="/media/javascript-images/javascript-15/api2.png" alt="apis">


---

#### Different types of APIs
<img style="height: 500px" src="/media/javascript-images/javascript-15/api3.png" alt="apis">


---

#### Different types of APIs
<img width="800" src="/media/javascript-images/javascript-15/api4.png" alt="apis">


---

#### REST

* REST is acronym for REpresentational State Transfer.
* REST is a set of of rules about how to use the HTTP protocol.
* RESTful Web services, provide interoperability between computer systems on the Internet.
* When a RESTful API is called, the server will transfer to the client a representation of the state of the requested resource.


---

#### <a href="https://restfulapi.net/rest-architectural-constraints/">REST Architectural Constraints</a>


---

#### What is an RESTful API?

* It's an interface or communication protocol between a client and a server.
* It's like a “contract” between the client and the server.
  * If the client makes a request in a specific format.
  * It will always get a response in a specific format.
  * Or initiate a defined action.
		 



---

#### Client & resource

* Client — the client is the person or software who uses the API.
* Resource — a resource can be any object the API can provide information about.
* The client then uses the servers API to get the resource.
* The API isn’t the same as the remote server — rather it is the part of the server that receives requests and sends responses.


---

#### Client & resource
<img src="/media/javascript-images/javascript-15/cr1.png" alt="rest">


---

#### Client & Resource & API
<img src="/media/javascript-images/javascript-15/cr2.png" alt="rest">


---

#### API URI (Uniform Resource Identifier)
<img src="/media/javascript-images/javascript-15/cr3.png" alt="rest">


---

#### API
<img src="/media/javascript-images/javascript-15/cr4.png" alt="rest">


---

#### API endpoints
<img src="/media/javascript-images/javascript-15/cr5.png" alt="rest">


---

#### Spotify API example

* Client: Your application
* Resource: Songs, playlists or users.
* Each resource has a unique identifier.
* API endpoint -> https://api.spotify.com/v1/artists/234/albums?album_type=SINGLE&limit=10
* Making the http request above will result in that Spotify will give you maximum 10 albums from a specific artist.


---

#### Example API's

* <a href="https://jsonplaceholder.typicode.com/">JSONplaceholder</a>
* <a href="https://developer.github.com/v3/">Github API</a>
* <a href="https://developer.spotify.com/documentation/web-api/">Spotify API</a>
* <a href="https://www.pexels.com/api/">Pexels API</a>


---

#### Using APIs we cannot just ask for and GET data(resources) we can also, send, update and delete data.


---

#### These are called CRUD operations

* CREATE
* READ
* UPDATE
* DELETE


---

#### CRUD operations

* Depending on in which system they are used they are called different things.

<img width="600" src="/media/javascript-images/javascript-15/crud.png" alt="CRUD operations">


---

#### The GET method

* GET is used to request data from a specified resource.
* Along with GET request we can send additional information about what we want to recieve using query strings.
* These are name/value pairs and are sent in the URL of a GET request.
* Start with ```?``` and seperated by ```&```

```JavaScript
'http://www.testing.com/test/demo_form.php?name1=value1&name2=value2'
```


---

#### The POST method

* POST is used to send data to a server to create/update a resource.
* The data sent to the server with POST is stored in the request body of the HTTP request.


---

#### Network tab
<img src="/media/javascript-images/javascript-15/nw.png" alt="network">


---
#### Network tab
<img src="/media/javascript-images/javascript-15/nw1.png" alt="network">


---
#### Network tab
<img src="/media/javascript-images/javascript-15/nw2.png" alt="network">


---
#### Network tab
<img src="/media/javascript-images/javascript-15/nw3.png" alt="network">


---
#### Network tab
<img src="/media/javascript-images/javascript-15/nw4.png" alt="network">


---

#### HTTP Headers

* HTTP headers let the client and the server pass additional information with an HTTP request or response.
* An HTTP header consists of its case-insensitive name followed by a colon (:), then by its value.
* Content-Type: application/json


---

#### Modern browsers support two different APIs for making HTTP requests

* <u>XMLHttpRequest (the focus of this lecture).</u>
* Fetch API (comes later in the course).


---

#### The XMLHttpRequest Object

* The XMLHttpRequest Object is used to exchange data with a server behind the scenes.
* This is done without reloading the whole page.

```JavaScript
// Creating an new XMLHttpRequest object
let xhr = new XMLHttpRequest();

// (<method>, <url>, <if asynchronos>)
xhr.open('GET', 'https://jsonplaceholder.typicode.com/todos/1', true);

// Sets how to handle the response
xhr.addEventListener('load', function(){
	if (this.readyState == 4 && this.status == 200) {
		console.log(this);  // Whole response object
		console.log(this.responseText);  // The response data
		JSON.parse(this.responseText); // Parses the JSON to a workable JavaScript object
	}
});

// Sends the request
xhr.send();
}
```


---

#### Common HTTP response status codes

* 200 OK (The request has succeeded)
* 400 Bad Request (This response means that server could not understand the request due to invalid syntax.)
* 401 Unauthorized
* 403 Forbidden
* 404 Not Found (The server can not find requested resource.)
* 500 Internal Server Error (The server has encountered a situation it doesn't know how to handle.)
* <a href="https://developer.mozilla.org/sv-SE/docs/Web/HTTP/Status" target="_blank">Full list</a>


---

#### XMLHttpRequest Readystates

* 0 UNSENT Client has been created. ```open()``` not called yet.
* 1 OPENED ```open()``` has been called.
* 2 HEADERS_RECEIVED ```send()``` has been called, and headers and status are available.
* 3 LOADING Downloading; responseText holds partial data.
* 4 DONE The operation is complete.


---

#### Check example code on how to use CRUD operations using REST


---

#### Access Across Domains

* For security reasons, modern browsers do not allow access across domains.
* Meaning that browsers do not load AJAX responses from servers thats not your own.
* This means that both the web page and the XML file it tries to load, must be located on the same server.
* However there are workarounds.


---

#### Workarounds

* Having a backend document on your server that requests the external data and then have that deliver the content.
* <a href="https://www.w3schools.com/js/js_json_jsonp.asp" target="_blank">JSONP</a> script tag instead to load external data.
* <a href="https://developer.mozilla.org/en-US/docs/Web/HTTP/CORS" target="_blank">CORS</a> - CROSS-ORIGIN RESOURCE SHARING
  * Set specific rules via HTTP headers to say that the communication between server and website is ok.


---

### <a href="https://github.com/SofthouseVxo/Education" target="_blank">Github examples!</a>