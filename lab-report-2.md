# Lab Report 2
## Introduction
This lab report focuses on creating a simple search engine using queries, as well as bug/symptom testing.




## Part I: Search Engine 
In regards to the search engine, the two queries we focused on were `/add` and `/search`, in which the former would add whatever element came afterwards into a list, and the latter would be able to pull up any element in the list that contained the string. 

If we ignore the packages imported, as well as everything else that did not relate to the functions of the search engine itself, the code is this:
```
class Handler implements URLHandler {
    ArrayList<String> listOfStrings = new ArrayList<String>();
    ArrayList<String> results = new ArrayList<String>();

    public String handleRequest(URI url) {
        if (url.getPath().equals("/search")) {
            String[] parameters = url.getQuery().split("=");
            if (parameters[0].equals("s")) {
                for (int i = 0; i < listOfStrings.size(); i++) {
                    if (listOfStrings.get(i).contains(parameters[1])) {
                        results.add(listOfStrings.get(i));
                        }
                    }
                String resultList = "";
                resultList = String.join("\n", results);
                return String.format("Found %d results:\n%s", results.size(), resultList); 
            }
            else {
                return "No element specified to search for!";
            }
        }
        if (url.getPath().equals("/add")) {
            System.out.println("Path: " + url.getPath());
            String[] parameters = url.getQuery().split("=");
            if (parameters[0].equals("s")) {
                listOfStrings.add(parameters[1]);
                return String.format(parameters[1] + " has been added to the list!");
            }
            return "No element specified to add!";
        }
        else {
            return "Simple Search Engine!";
        }
    }
}
```
This code goes through queries and adds elements to a separate list called `listOfStrings`, and then iterates through it to find any element that contains the desired string.


Some examples of the code being implemented are:

![Image](Screenshot9.png)

![Image](Screenshot10.png)

![Image](Screenshot11.png)

In the images above, "apple", "pineapple", and "anewstringtoadd" are being added to the `listOfStrings`. This calls several methods: 
* `.add(String e)` --> `listofStrings.add(parameters[1])`, in which everything after the equal sign (=) in the URL is being added to the `listOfStrings`.
* `.getPath()`
* `.getQuery()`
* `.split(String regex)` --> `url.getQuery().split("=")`, in which `String[] parameters` is assigned the query of the URL.
* `.equals(Object anObject)` --> `parameters[0].equals("s")`, in which the condition is met if the specified part of the URL contains the letter "s", and `url.getPath().equals("/add")` fulfills the condition if the URL path equals "/add".
* `.format(String format, Object... args)` --> `String.format(parameters[1] + " has been added to the list!")`, which prints out what element has been added to the list for confirmation in proper format.

None of these values change, as it is simply adding a string into an arraylist of strings. 

![Image](Screenshot12.png)
In this image, the desired search is "app", which results in "apple" and "pineapple", and not "anewstringtoadd" since it does not contain what was searched. It iterates through the `listOfStrings` to find which strings contain the parameter given. This also calls several methods: 
* `.add(String e)` --> `results.add(listOfStrings.get(i))`, in which everything that contains the parameter is added to a new arraylist for printing.
* `.getPath()`
* `.contains(CharSequence s)` --> `listOfStrings.get(i).contains(parameters[1])`, in which the condition is met if the URL contains the specified parameter.
* `.getQuery()`
* `.split(String regex)` --> `url.getQuery().split("=")`, in which `String[] parameters` is assigned the query of the URL.
* `.equals(Object anObject)` --> `parameters[0].equals("s")`, in which the condition is met if the specified part of the URL contains the letter "s". 
* `.format(String format, Object... args)` --> `String.format("Found %d results:\n%s", results.size(), resultList)`, which prints out how many elements and which have been found to contain the parameter. 
* `.join(CharSequence delimiter, Iterable <? extends CharSequence> elements)` --> `String.join("\n", results)`, in which resultList is assigned to this and now prints every element that fits the search in separate rows.

These values, similarly, do not change as they are strings being added to a singular string, only separated in lines.

***

## Part II: Bugs/Symptoms 




The failure-inducing input (the code of the test)
The symptom (the failing test output)
The bug (the code fix needed)
Then, explain the connection between the symptom and the bug. Why does the bug cause that particular symptom for that particular input?