# ModuleManager Tutorial for Complete Beginners - Lesson 2 - ModuleManager Basics

Edit or Create - ```%```
The Edit or Create prefix edits the node/value if it exists, but if it doesnt, the node/value is created
```
@PART[fueltank1]
{
        @title = thy
        %techRequired = basicRocketry
}
```
`%techRequired = basicRocketry` checks to see if `techRequired` exists. If it does, it is edited as if we were using the `@` prefix. If it doesnt, `techRequired = basicRocketry` was added as if there was no prefix at all. 
