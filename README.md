# PHP-with-OOP-and-JSON-PHP-with-OOP-and-XML.IPRC NGOMA 
DEPARTEMENT OF ICT
OPTION OF IT
CLASS: ITLevel7/Year 3
Module Title: Advanced Web Technologies
Module Code: ITLAW701
Group 7: GROUP MEMBERS
1.	DUKUZUMUREMYI Albert  20RP10374
2.	DUSHIMIMANA Samuel    20RP03103
3.	SIBO Patrick          20RP12254

PHP and MySQL Assignment (Duration: 2weeks, not later than June 20th, 2023)
1.	By using PHP with OOP and Ajax, describe into details with a concrete example of your choosing the following technical terms: XMLHttpRequest Object, Creating XMLHttpRequest Object, sending a Request to a Server, Receiving response from server and the onreadystatechange Event.
      a) XMLHttpRequest Object: The XMLHttpRequest object is a built-in JavaScript object that allows client-side web applications to make HTTP requests to a server asynchronously without reloading the entire web page. It is commonly used in conjunction with Ajax to update parts of a web page dynamically.
b) Creating XMLHttpRequest Object: In PHP with OOP and Ajax, you can create an XMLHttpRequest object using JavaScript. Here's an example of creating an XMLHttpRequest object:
var xhttp = new XMLHttpRequest();
c) Sending a Request to a Server: Once you have created an XMLHttpRequest object, you can use it to send a request to a server. Here's an example of sending a GET request to a server using the XMLHttpRequest object:
 xhttp.open("GET", "example.php", true);
xhttp.send();
In the above code, we use the open() method to specify the HTTP method ("GET" in this case), the URL of the server-side script ("example.php"), and whether the request should be asynchronous (true in this case). Then, we use the send() method to send the request to the server.
d) Receiving Response from Server: After sending a request to the server, we need to handle the response received from the server. We can do this by defining a callback function that gets executed when the server response is ready. Here's an example:
xhttp.onreadystatechange = function() {
  if (xhttp.readyState === XMLHttpRequest.DONE && xhttp.status === 200) {
    var response = xhttp.responseText;
    // Handle the response here
  }
};


    In the above code, we assign an anonymous function to the onreadystatechange event of the XMLHttpRequest object. The function checks if the readyState is XMLHttpRequest.DONE (which means the request is complete) and the status is 200 (which indicates a successful response). If the conditions are met, we can access the response from the server using the responseText property of the XMLHttpRequest object.
e) The onreadystatechange Event: The onreadystatechange event is triggered whenever the readyState property of the XMLHttpRequest object changes. It allows us to define a function that will be executed each time the state changes. This event is commonly used to handle the response from the server. In the previous example, we assigned a callback function to the onreadystatechange event.

2.	Use PHP with OOP and JSON, describe into details with a concrete example of your choosing.
  PHP with OOP and JSON:
In PHP, you can use object-oriented programming (OOP) to work with JSON data. Here's a concrete example:
class User {
  public $name;
  public $email;
  public $age;

  public function __construct($name, $email, $age) {
    $this->name = $name;
    $this->email = $email;
    $this->age = $age;
  }

  public function toJSON() {
    return json_encode($this);
  }
}

$user = new User("John Doe", "john@example.com", 25);
$jsonData = $user->toJSON();

echo $jsonData;

 In the above code, we define a User class with properties for name, email, and age. The class has a constructor to initialize these properties. Additionally, we have a toJSON() method that converts the user object to JSON using the json_encode() function. Finally, we create an instance of the User class and call the toJSON() method to get the JSON representation of the user object. The JSON data is then echoed.

3.	Use PHP with OOP and XML, describe into details with a concrete example of your choosing.
  PHP with OOP and XML:
In PHP, you can also use object-oriented programming (OOP) to work with XML data. Here's a concrete example:
class Book {
  public $title;
  public $author;
  public $year;

  public function __construct($title, $author, $year) {
    $this->title = $title;
    $this->author = $author;
    $this->year = $year;
  }

  public function toXML() {
    $xml = new SimpleXMLElement('<book></book>');
    $xml->addChild('title', $this->title);
    $xml->addChild('author', $this->author);
    $xml->addChild('year', $this->year);

    return $xml->asXML();
  }
}

$book = new Book("The Great Gatsby", "F. Scott Fitzgerald", 1925);
$xmlData = $book->toXML();

echo $xmlData;

    In the above code, we define a Book class with properties for title, author, and year. The class has a constructor to initialize these properties. We also have a toXML() method that creates a new SimpleXMLElement object and adds child elements for title, author, and year. The asXML() method is then used to convert the XML object to a string. Finally, we create an instance of the Book class and call the toXML() method to get the XML representation of the book object. The XML data is then echoed.
  
                                                            ---- END ----
