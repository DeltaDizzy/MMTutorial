# ModuleManager Tutorial for Complete Beginners - Lesson 2 - MM Basics

ModuleManager, commonly abbrviated as MM, allows you to edit ConfgNodes without overwriting them. The system for doing this is incedibly simple, consisting of 4 command symbols and 4 filters. MM also includes square brackets (`[]`). If the node you are diting includes a `name` value, you can use them to specify the node to edit. For example:
```
NODE
{
    name = rty
}
NODE
{
    name = ruy
}
@NODE[ruy] //Edits the second node from the top, since its name matches the value in square brackets
{
}
```
