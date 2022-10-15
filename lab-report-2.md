# Lab Report 2

## Part 1: Simplest Search Engine 
```
import java.io.IOException;
import java.net.URI;
import java.util.ArrayList;

class Handler implements URLHandler {
    // The one bit of state on the server: a number that will be manipulated by
    // various requests.

    ArrayList<String> listString = new ArrayList<>();

    public String handleRequest(URI url) {
        if (url.getPath().equals("/")) {
            return String.format("Number: %d", listString.toString());
        } else {
            System.out.println("Path: " + url.getPath());
            if (url.getPath().contains("/add")) {
                String[] parameters = url.getQuery().split("=");
                if (parameters[0].equals("s")) {
                    listString.add(parameters[1]);
                    return String.format("Added String by %s! List now contains %d strings", parameters[1], listString.size());
                }
            }
            else if(url.getPath().contains("/search")){
                String[] parameters = url.getQuery().split("=");
                if (parameters[0].equals("s")){
                    ArrayList<String> toReturn = new ArrayList<>();
                    for(String s: listString){
                        if (s.contains(parameters[1])) {
                            toReturn.add(parameters[1]);
                        }
                    }
                    return String.format("%d strings found matching query. Stings are by %s", toReturn.size(), toReturn.toString());
                }

            }

             

            return "404 Not Found!";
        }
    }

}

class SearchEngine {
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


## Finding Bugs 

Bug 1: ArrayExamples 
![fail_input_image](Bug1_fail_input.png)
The code above is the test case I wrote which caused the bug to display a symptom

![fail_output_image](Bug1_fail_ouput.png)
The screenshot above shows the symptoms of the failure inducing code   

![bug_location_image](Bug%201_location.png)

Here is the part of the code which causes the symptoms to appear

Bug Explanation:  
The connection between the bug and the symptom is seen clearest when we look at the latter half of the output array. There we can see that for an input array of {1,2,3,4,5} that the output is {5,4,3,4,5} instead of {5,4,3,2,1}. We can see that in the terminal it alerts us that the test failed at element <3>, where we wrote a test to expect the third element to have a value of 2 but instead it was 4. Upon looking at the code we can find the bug to be that as we iterate through the input we are actively overwriting the array at the same time. This causes the input to be updated as we progress through each element causing the output to be off once we reach the midpoint of the array. To fix this bug we need to save the input array as a variable and then store the output array as its own variable. That way we do not overwrite the earlier elements when we iterate through the input array to reverse the array. 

