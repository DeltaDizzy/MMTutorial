# ModuleManager for Complete Beginners - Lesson 6 - Copy

Sometimes you will want to use a preexisting node as a kind of template. Here's an example from one of my mods. It adds a converter module to the stock ISRU parts.
```
@PART[ISRU,miniISRU]:NEEDS[GeOdysseyCOr]
{
	//Copy the Mono Converter Module
    +MODULE[ModuleResourceConverter]:HAS[#ConverterName[Mono*]]
    {
        @ConverterName = Zenon Liberator
        @StartActionName = Start Heaters
        @StopActionName = Stop Output Pumps
        
        //Purge the module of inputs and outputs on copy. Will not harm/delete other converter modules themselves
        -INPUT_RESOURCE,* {}
        -OUTPUT_RESOURCE,* {}
        
        //Add the Zenon resource chain
        INPUT_RESOURCE
        {
            ResourceName = Zenon
            Ratio = 2.5
            FlowMode = STAGE_PRIORITY_FLOW
        }
        INPUT_RESOURCE
        {
            ResourceName = ElectricCharge
            Ratio = 30
        }
        OUTPUT_RESOURCE
        {
            ResourceName = XenonGas
            Ratio = 105
            DumpExcess = false
            FlowMode = STAGE_PRIORITY_FLOW
        }
    }
```
Most of that should make sense to you, and I promise, `:HAS[]` is coming up real soon.

Copying nodes and values works in much the same way as deleting them, hwever when you copy a node, you can apply commands to any fields in it.
