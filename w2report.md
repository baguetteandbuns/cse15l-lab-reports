# Week 2 Lab Report
## Part 1
* Code for `StringServer.java`:

`import java.io.IOException;
import java.net.URI;

class Handler implements URLHandler {
    // The one bit of state on the server: a number that will be manipulated by
    // various requests.
    int num = 0;
    String text = "";

    public String handleRequest(URI url) {
        if (url.getPath().equals("/")) {
            return "enter String";
        } else if (url.getPath().equals("/add-message")) {
            String[] parameters = url.getQuery().split("=");
                if (parameters[0].equals("s")) {
                    text = text + "\n" + parameters[1];
                    return text;
                }
        } 
            return "404 Not Found!";
        }
    
}

class StringServer {
    public static void main(String[] args) throws IOException {
        if(args.length == 0){
            System.out.println("Missing port number! Try any number between 1024 to 49151");
            return;
        }

        int port = Integer.parseInt(args[0]);

        Server.start(port, new Handler());
    }
}`

* I ran the file and started the server using the following commands in the terminal:
<img width="592" alt="Screenshot 2023-01-28 at 3 07 08 PM" src="https://user-images.githubusercontent.com/122561814/215295215-81c58183-5272-4176-b726-10c7b575cbc3.png">

### Screenshot 1
* When I opened the website using the following URL: [http://localhost:4000/add-message?s=Hello](http://localhost:4000/add-message?s=Hello), this was the result:

<img width="433" alt="Screenshot 2023-01-28 at 3 02 52 PM" src="https://user-images.githubusercontent.com/122561814/215295128-1b46e6da-57ef-4fdd-b814-11ee39096253.png">
* The main method in the `StringServer` class and the handleRequest method in the `Handler` class is called upon 
* 

<img width="525" alt="Screenshot 2023-01-28 at 3 03 13 PM" src="https://user-images.githubusercontent.com/122561814/215295131-f0c2758b-b74c-4c0d-8ee6-b7aa81000c0c.png">

## Part 2
* Method with Bug Chosen: `ArrayExamples.reversed()`
* An input that does induce a failure, as a JUnit test:

`@Test
  public void testReversed2(){
    int[] input1 = {3, 2};
    assertArrayEquals(new int[]{2, 3}, ArrayExamples.reversed(input1));
  }`
* An input that doesn’t induce a failure, as a JUnit test:

`@Test
  public void testReversed() {
    int[] input1 = { };
    assertArrayEquals(new int[]{ }, ArrayExamples.reversed(input1));
  }`
 * Result of JUnit Tests before fixings bugs:
<img width="960" alt="Screenshot 2023-01-28 at 3 27 27 PM" src="https://user-images.githubusercontent.com/122561814/215295763-eae03853-3b8d-4de7-b5b6-9b95ad08915f.png">


 * Result of JUnit Tests after fixing bugs:
  <img width="962" alt="Screenshot 2023-01-28 at 3 24 08 PM" src="https://user-images.githubusercontent.com/122561814/215295657-5184936b-d045-4c05-aff8-6393de3bceba.png">

* Code Before fixing Bug: 
`static int[] reversed(int[] arr) {
    int[] newArray = new int[arr.length];
    for(int i = 0; i < arr.length; i += 1) {
      arr[i] = newArray[arr.length - i - 1];
    }
    return arr;
  }`
* Code After fixing Bug:

`static int[] reversed(int[] arr) {
    int[] newArray = new int[arr.length];
    for(int i = 0; i < arr.length; i += 1) {
      newArray[arr.length - i-1] = arr[i];
    }
    return newArray;
  }`
  
* Brief Description of Bug Solving: the old code assigns an element value from the new array (which is empty) into the input array, rather than the input array assigning a value to the new array. I reversed the assignment of the elements, which fixed the bug. 
## Part 3
* I didn't know how to start servers before week 2
* I didn't know what queries are and how they are interpreted. I learnt to use the `.getQuery()` method and `.split()` method that helped me implement string concatenation and number addition of the URL
* I learnt that difference between URL and URI during lab
* I wasn't very comfortable with using JUnit before week 3's lab
