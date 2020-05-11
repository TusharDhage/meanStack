# JS Object:-
  - Objects are values that can contain other values. They use keys to name values, which are a lot like variables.
 
*EXAMPLE*:

       var course = {
       
            name: "GRA 2032",
            
            start: 8,
            
            end: 10
            
                    };
___
## Getting keys

To get an object’s key, you have two options:

> 1.You can use dot notation with the name of the key after a period ..

*EXAMPLE*

var course = {

       name: "GRA 2032",
       
       start: 8,
       
       end: 10
       
};

`course.name`;

*OUTPUT*:- "GRA 2032"

> 2.Or you can use bracket notation with the name of the key inside a string inside square brackets [""].

*EXAMPLE*

var course = {

       name: "GRA 2032",
       
       start: 8,
       
       end: 10
};

`course["name"]`;

*OUTPUT*:- "GRA 2032"
___
## Setting keys

- To add keys to an object or overwrite its keys, you have the same two options as getting its keys.

> 1.You can use dot notation with the name of the key after a period and an equals sign =.

*EXAMPLE*:-

var character = {

       name: "Donna",
       
       hair: "red"
       
};

`character.hair = "blonde"`;

character;

*OUTPUT*:-
{
       "name": "Donna",
       
       "hair": "blonde"
}

> 2.you can use bracket notation with the name of the key inside a string inside square brackets [""] and an equals sign =.

*EXAMPLE*

var character = {

       name: "Donna",
       
       hair: "red"
       
};
`character["hair"] = "blonde"`;

character;

*OUTPUT*:-
{

       "name": "Donna",
       
       "hair": "blonde"
       
}
























