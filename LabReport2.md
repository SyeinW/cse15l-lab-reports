# Part 1

```
import java.io.IOException;
import java.net.URI;

class Handler implements URLHandler {
    String messages = "";
    public String handleRequest (URI url) {
        System.out.println("Path: " + url.getPath());
        if (url.getPath().contains("/add-message")) {
            String [] parameters = url.getQuery().split("=");
            if (parameters[0].equals("s")) {
                messages = messages + parameters[1] + "\n";
                return messages;
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
}
```

![image](https://user-images.githubusercontent.com/113940184/215656795-3e7d920d-467f-4ca9-a445-e3a942af6ad4.png)

* I only have one method ```handleRequests()``` and in the case of the image above, it is called twice. It was first called when I put the query ```/add-message?s=Hi, my name is Shane West!``` and a second time when I put the query ```/add-message?s="Start early, start often" - Paul Cao```. 
* The single argument of ```handleRequests()``` is the URL we type in. So in the aforementioned cases the ```handleRequests()``` method took in ```/add-message?s=Hi, my name is Shane West!``` & ```/add-message?s="Start early, start often" - Paul Cao``` respectively, as an argument. I instantiated an empty String object named ```messages``` with the purpose to store and concatenate the text from derived from the query. 
* With the first call of ```handleRequests()``` the String ```messages``` is updated from an empty string to a String containing ```"Hi, my name is Shane West!"``` and a new line is concatenated. The String array ```parameters``` has each of its indexes set to a certain part of the original url. ```[0]``` is = s and ```[1]``` is = ```"Hi, my name is Shane West!"```. The second call is almost exactly the same except the string is updated to include ```"Start early, start often" - Paul Cao"``` instead of ```"Hi, my name is Shane West!"```.

![image](https://user-images.githubusercontent.com/113940184/215656565-b981a32a-3d2a-471b-916b-6c34c908127b.png)

* Similar to image 1, we are only calling ```handleRequests()```
* In this case, we didn't enter anything after ```/add-message``` so when we call ```url.getQuery().split("=")``` the compiler throws an error because our query is ```= null``` 
* No values got changed since java threw an error 


# Part 2

## Failed JUnit test

```   
  @Test
  public void testReversed() {
    int[] input1 = { };
    int[] input2 = {1, 2, 3 };
    assertArrayEquals(new int[]{ }, ArrayExamples.reversed(input1));
    assertArrayEquals(new int[]{3, 2, 1}, ArrayExamples.reversed(input2));
```

## Incorrect Pass test

```
  @Test
  public void testReversed() {
    int[] input1 = { };
    int[] input2 = {0, 0, 0};
    assertArrayEquals(new int[]{ }, ArrayExamples.reversed(input1));
    assertArrayEquals(new int[]{0, 0, 0}, ArrayExamples.reversed(input2));

  }
```

## Symptom

![image](https://user-images.githubusercontent.com/113940184/215661997-4aed813b-2f19-498a-a7d2-a3878a781fcf.png)

## Bug Before

```
  static int[] reversed(int[] arr) {
    int[] newArray = new int[arr.length];
    for(int i = 0; i < arr.length; i += 1) {
      arr[i] = newArray[arr.length - i - 1];
    }
    return newArray;
  }
```

# Bug After

```
  static int[] reversed(int[] arr) {
    int[] newArray = new int[arr.length];
    for(int i = 0; i < arr.length; i += 1) {
      newArray[i] = arr[arr.length - i - 1];
    }
    return newArray;
  }
```
The original code was setting the array ```arr``` indexes equal to the empty array ```newArray``` indexes. The key problem here is that ```newArray``` was empty. So copying from the empty array just made the original array ```arr``` and empty array. By switching the positions of ```arr``` and ```newArray``` in line 4 we correct this mistake. Allowing for the non-empty array ```arr``` to copy over a reversed version onto the empty array ```newArray```.

# Part 3

