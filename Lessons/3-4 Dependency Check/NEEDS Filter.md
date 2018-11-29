# ModuleManager for Complete Beginners - Lesson 3.4 - Depedency Checking with NEEDS

If you are patching a mod, you want to make sure it is actually installed. You can do this with the NEEDS filter.

```
@NODE:NEEDS[FolderOrDLLName]
{

}
```
If you want to patch a mod that exists in GameData/myModA, you would use `NEEDS[myModA]`. If it had a .dll file named myModADD.dll, you could also use `NEEDS[myModADD]`.
