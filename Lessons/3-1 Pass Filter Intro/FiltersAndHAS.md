# ModuleManager for Comlete Beginners - Lesson 3.1 - Filters

```
@PART:HAS[@MODULE[ModuleCommand] && #cost[500]]
{
  MODULE
  {
    name = ModulBlankName //Not a real module
  }
}
```

Say you want to apply a patch to all parts that have a particular module or that have a prticular value for a certain key. You can do this using pass filters. In past versions of MM, you needed to use `@PART[*]`, but now `@PART` as the same function.
To specify a pass filter or check, use `:PASSNAME[Input]`. possible pass names are HAS, AFTER, BEFORE, and NEEDS. This lesson will focus on HAS. 

Filters are boolean operations, and the patch will only run if it evaluates to true. to include a module, put `@MODULE[ModuleName]` inside `HAS[]`. Including a node means it will only be applied to parts _**WITH**_ a module named ModuleName. To exclude a node, which will apply the patch only to parts _**WITHOUT**_ the module), use `!MODULE[ModuleName]. For example:

To include keys, put `#keyName[value]`. It will then only apply the patch to parts with a key named `keyName` that is equal to `value`.

You can combine any number of keys and/or nodes in one `HAS[]` filter.
