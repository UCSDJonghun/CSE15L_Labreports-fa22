## Search Engine

import java.io.IOException;
import java.net.URI;
import java.util.ArrayList;
#
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
