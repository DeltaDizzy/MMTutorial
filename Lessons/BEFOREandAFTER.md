# ModuleManager for Complete Beginners - Lesson 3.3 - Load Order Filters

Two of the pass filters control when patches are applied. They are `BEFORE[ModName]` and `AFTER[ModName]`. AFTER is used when you want to patch a mod that loads before your patch, due it being earlier in alphabetical order. BEFORE is the opposite, and is incredibly rare. A common example is planet configs for Kopernicus, which use AFTER because they edit the `Kopernicus` node included with Kopernicus.

```
@Kopernius:AFTER[Kopernicus]
{
  Body
  {
    //wow what a nice planet
  }
}
```
