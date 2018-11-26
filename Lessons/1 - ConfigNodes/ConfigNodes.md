# ModuleManager Tutorial - Lesson 1 - ConfigNodes

KSP uses a format called ConfigNodes to store information about parts, science reports, and more. You will use them to edit things in KSP without overwriting the default files. Firstly though, we must learn the structure of a ConfigNode. A ConfigNode can contain 2 types of information: Values and Nodes. A value is a simple variable, such as "name = thing"  or "x = 7". A node is jsut another ConfigNode, which can contain its own values and nodes, and this can continue on hypothetically forever, though it is very rare to have more than 3 layers of nodes. Value name are typically camelCase (first 'word' of name is lowercase, first letter of every word after it is uppercase), and node names are usually all caps(LIKE_THIS) while they can also be UpperCamelCase(LikeThis). Comments are lines that are not read by the game code, and are used to hold notes or text from the programmer. To create a comment, type `//`. Everything after `//` will be ignored Here is an example:

```
PART
{
	name = partName
	// other part values
	MODULE
	{
		name = ModuleCommand
		//module fields
		//fields and values are the same thing
	}
}
```
