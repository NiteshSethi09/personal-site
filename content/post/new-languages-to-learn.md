---
title: "4 Programming Languages Worth Trying"
date: "2019-06-23"
description: 4 languages that can help you to become a better programmer and expand your experience.
---

Learning new programming language is very satisfying and fulfilling experience. Learning new programming language helps you to see programming in very different prespectives. It shows you different methods to solve same problems. Trying languages that uses unfamiliar concepts is good things because in the end you get experience that you wouldn't get otherwise.

Here are some programming languages that I think every one should try once.

### 1. Smalltalk
![smalltalk image](/img/smalltalk.jpeg)

_Image from Byte Magazine Vol. 6 No. 8 cover, August 1981_

Smalltalk is a  object-oriented, dynamically typed language which have inspired an array of modern languages. Smalltalk has very noble ideas but unfortunately It never become mainstream language.

Features of Smalltalk:

1.  Smalltalk provides a live & incremental development environment.
2. Smalltalk is most productive programming language. [1]
3.  It is a pure OO language, with objects all the way down.

```

"Compute difference in days between two dates"
('2014-07-01' asDate - '2013/2/1' asDate) days

"Return the weekday of a date"
'2013/5/7' asDate dayOfWeekName

"Save the HTML source of a web page to a file"
'http://www.pharo.org' asUrl saveContentsToFile: 'page.html'

"Count the number of, or show the leap years between two years"
(1914 to: 1945) count: [ :each | Year isLeapYear: each ].
(1895 to: 1915) select: [ :each | Year isLeapYear: each ].
```

It you want to try smalltalk you can learn the basic syntax from [Learn Smalltalk with ProfStef ](https://amber-lang.net/learn.html). [Pharo](https://pharo.org) is famous smalltalk other than that [Amber](https://amber-lang.net/) is a smalltalk varient that compiles to javascript.

### 2. SQL

Structured Query Language, is used to interface with databases. If you use ORM to interact with database then SQL will be going a little low level. SQL syntax vary little between different RDMS but it's mostly the same.

Actually SQL is pretty small language you can finish the most part in weekends.

``` 

-- Select all rows and columns from the current database's departments table.
-- Default activity is for the interpreter to scroll the results on your screen. 
SELECT * FROM departments;

-- Retrieve all rows from the departments table, 
-- but only the dept_no and dept_name columns. 
-- Splitting up commands across lines is OK.
SELECT dept_no, dept_name FROM departments;

-- Create a table called tablename1, with the two columns shown, for
-- the database currently in use. Lots of other options are available
-- for how you specify the columns, such as their datatypes.
CREATE TABLE tablename1 (fname VARCHAR(20), lname VARCHAR(20));

-- Insert a row of data into the table tablename1. This assumes that the 
-- table has been defined to accept these values as appropriate for it. 
INSERT INTO tablename1 VALUES('Richard','Mutt');

-- In tablename1, change the fname value to 'John'
-- for all rows that have an lname value of 'Mutt'. 
UPDATE tablename1 SET fname='John' WHERE lname='Mutt';
```

### 3. Go
![golang image](/img/golang.png)

_Image from [Learning Go — from zero to hero
](https://www.freecodecamp.org/news/learning-go-from-zero-to-hero-d2a3223b3d86/)_

Go is very simple language. It compiles to native code and offers builtin concurrency. Go is really nice language to make web servers. It's major benefits are:

1. Readable and productive syntax
2. Built-in concurrency
3. Fast compilation times
4. Static typing
5. Garbage collection built-in
6. binaries that are simple to deploy

```

// Writing a basic HTTP server is easy using the
// `net/http` package.
package main

import (
    "fmt"
    "net/http"
)

// A fundamental concept in `net/http` servers is
// *handlers*. A handler is an object implementing the
// `http.Handler` interface. A common way to write
// a handler is by using the `http.HandlerFunc` adapter
// on functions with the appropriate signature.
func hello(w http.ResponseWriter, req *http.Request) {

    // Functions serving as handlers take a
    // `http.ResponseWriter` and a `http.Request` as
    // arguments. The response writer is used to fill in the
    // HTTP response. Here out simple response is just
    // "hello\n".
    fmt.Fprintf(w, "hello\n")
}

func headers(w http.ResponseWriter, req *http.Request) {

    // This handler does something a little more
    // sophisticated by reading all the HTTP request
    // headers and echoing them into the response body.
    for name, headers := range req.Header {
        for _, h := range headers {
            fmt.Fprintf(w, "%v: %v\n", name, h)
        }
    }
}

func main() {

    // We register our handlers on server routes using the
    // `http.HandleFunc` convenience function. It sets up
    // the *default router* in the `net/http` package and
    // takes a function as an argument.
    http.HandleFunc("/hello", hello)
    http.HandleFunc("/headers", headers)

    // Finally, we call the `ListenAndServe` with the port
    // and a handler. `nil` tells it to use the default
    // router we've just set up.
    http.ListenAndServe(":8090", nil)
}
```

You can start learning go from [A Tour of Go](https://tour.golang.org) or [Learning Go — from zero to hero](https://www.freecodecamp.org/news/learning-go-from-zero-to-hero-d2a3223b3d86/)

### 4. Haskell
Haskell is a popular functional programming language. It forces you to think in a completely different ways. You will learn things like Monad, writing programs without state. I choose haskell intead of other functional languages because of its strong typing and abundance of free learning resources. 

```
-- A simple function that takes two variables
add a b = a + b

-- Note that if you are using ghci (the Haskell interpreter)
-- You'll need to use `let`, i.e.
-- let add a b = a + b

-- Using the function
add 1 2 -- 3

-- You can also put the function name between the two arguments
-- with backticks:
1 `add` 2 -- 3

-- if-expressions
haskell = if 1 == 1 then "awesome" else "awful" -- haskell = "awesome"

-- if-expressions can be on multiple lines too, indentation is important
haskell = if 1 == 1
            then "awesome"
            else "awful"

-- Here's how you make your own data type in Haskell

data Color = Red | Blue | Green

-- Now you can use it in a function:

say :: Color -> String
say Red   = "You are Red!"
say Blue  = "You are Blue!"
say Green = "You are Green!"
```

You can learn haskell from [Learn You a Haskell for Great Good!](http://learnyouahaskell.com/chapters)

