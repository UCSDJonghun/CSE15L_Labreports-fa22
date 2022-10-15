**Search Engine**
#
import java.io.IOException;
import java.net.URI;
import java.util.ArrayList;

class Handler implements URLHandler {
    ArrayList<String> terms = new ArrayList<String>();

    public String handleRequest(URI url) {
        if (url.getPath().equals("/"))
            return String.format("");
        else if (url.getPath().contains("/add")) {
            String[] parameters = url.getQuery().split("=");
            terms.add(parameters[1]);
            return String.format("Documented!");
        } else if (url.getPath().contains("/search")) {
            String s = "";
            String[] parameters = url.getQuery().split("=");
            for (int x = 0; x < terms.size(); x++) {
                if (terms.get(x).contains(parameters[1])) {
                    s += terms.get(x) + "\n";
                }
            }
            if (s.equals("")) {
                return String.format("We have found nothing");
            } else {
                return String.format("We found these: %s", s);
            }
        }
        return "404 not found!";
    }
}
class SearchEngine {
    public static void main(String[] args) throws IOException {
        if (args.length == 0) {
            System.out.println("Missing port number! Try any number between 1024 to 49151");
            return;
        }
        int port = Integer.parseInt(args[0]);
        Server.start(port, new Handler());
    }
}
                                             
                                          
## Screenshort                             
![image](https://user-images.githubusercontent.com/114322721/195969968-58b33225-4ba9-4052-9a23-ce03f9d0755d.png)
                                             
To add a word, you need to append /add?s=anewstringtoadd

/add?s=pineapple

/add?s=apple

/search?s=app= and the word to the end of the URL, and the word should be printed out on the website.
                                             
![image](https://user-images.githubusercontent.com/114322721/195970672-75e912d3-6f9a-4640-ae3a-a374123e6b01.png)
                                             
![image](https://user-images.githubusercontent.com/114322721/195970763-04a92f26-1617-48ea-994f-3799ce6c054e.png)

![image](https://user-images.githubusercontent.com/114322721/195970772-27cb2c62-491b-439c-992e-29858f041170.png)


![image](https://user-images.githubusercontent.com/114322721/195970711-d2984343-bbb3-4a9e-94cf-899ee4aece6a.png)

"/search?s=something" is finding word include in something word.

## Part2 

@Test
  public void testReversed1() {
    int[] input1 = { 3, 2, 1 };
    int[] output1 = ArrayExamples.reversed(input1);
    assertArrayEquals(new int[] { 1, 2, 3 }, output1);
  }
                                             
