# ModuleManager for Complete Beginners - Lesson 5 - Delete

The need to delte a node or value will come surprisingly often.  You can delete with 2 different symbols, `!` and `-`. To delete a value, set the value to anything while uing the delete prefix:
`!mass = DELETE`
`!mass = Billy Mays here, let me introduce you to another amazing product`
When Deleteing a node, specify the `name` value in square brackets and add 2 empty curly braces on the end.
Each symbol can be used anywhere the other can.

```
@PART[fueltank1] //lets make this hold xenon
{
  !RESOURCE[LiquidFuel] { }
  !RESOURCE[Oxidizer] { }
  
  RESOURCE
  {
    name = XenonGas
    amount = 77765
  }
}
```
