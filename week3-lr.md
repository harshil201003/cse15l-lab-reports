# Week 3 Lab Report


## Part 1 - Search Engine


The code for the Search Engine is:

```
import java.io.IOException;
import java.net.URI;
import java.util.ArrayList;


class SearchEngineMaker implements URLHandler
{
    ArrayList<String> added = new ArrayList<>();
    ArrayList<String> result= new ArrayList<>();
    public String handleRequest (URI url)
    {
        
        if (url.getPath().contains("/add")) 
        {
            String[] parameters = url.getQuery().split("=");
            if (parameters[0].equals("s"))
            {
            added.add(parameters[1]);
            return String.format("%b has been added!", parameters[1]);
            }
        }
        
        if (url.getPath().contains("/search")){
            String[] parameters = url.getQuery().split("=");
            
            if (parameters[0].equals("s"))
            {
                for (int i = 0; i < added.size(); i++)
                {
                    if (added.get(i).contains(parameters[1]))
                    {
                        result.add(added.get(i));
                    }
                }
                return result.toString();
            }  
        }

        return null;

    }
}

class SearchEngine
{
    public static void main(String[] args) throws IOException{
        if(args.length == 0){
            System.out.println("Missing port number! Try any number between 1024 to 49151");
            return;
        }

        int port = Integer.parseInt(args[0]);

        Server.start(port, new SearchEngineMaker());
    }
}
```


This code is a simple search engine that finds strings in the array of the website conting the key words. Strings can be added to the array of the Search Engine using the /add method in the query.


`/add?s=pineapple`  at the end of the query adds the string to the array.


![Pineapple](pine.png)


Another string is added here.


![Apple](addApple.png)


Now, to search, we replace /add with /search - 


![Search](search.png)



Talking about the code,



```
if (url.getPath().contains("/add")) 
    {
        String[] parameters = url.getQuery().split("=");
        if (parameters[0].equals("s"))
        {
            added.add(parameters[1]);
            return String.format("%b has been added!", parameters[1]);
        }
    }
```


The add function simply adds the string to an empty array called added. It splits the query of the URL into two strings. If the first element of the string is "s", it adds the second part of the string to the array. Once, the new String has successfully been added, it displays a confirmatory message on the website. 


The search path of the URL however, checks if the path contains "search". 


```
if (url.getPath().contains("/search")){
    String[] parameters = url.getQuery().split("=");

    if (parameters[0].equals("s"))
    {
        for (int i = 0; i < added.size(); i++)
        {
            if (added.get(i).contains(parameters[1]))
            {
                result.add(added.get(i));
            }
        }
        return result.toString();
    }  
}
```

Just like add, it separates the query into two and after the criteria for using search are met, it traverses through the "added" array and uses the get method to check if the words mentioned in the query of the URL match the ones in the array. Once this process is done, it returns the words that match.


The most important value of this code is the selection of the newly separated string's second argument. That is what defines what word needs to be added or searched. If that changes, there will be nothing to add. However, the first argument, the "s" before the equals makes sure that the argument being added is a string. So if that is changed, the if statement will fail and the code will not progress. 




