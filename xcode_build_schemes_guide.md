# Guide to create Test and live build schemes in Xcode  

## Target
Change target name to your schema name

### In General
Change **Display Name** to `$(PRODUCT_NAME)`  

### In build settings
Change bundle idendifier name
Check if there is DEBUG flag set in **Active Compilation Conditions** in **Swift Compiler - Custom Flags**  

## Schemes
Create different schemes, eg: **YourPrj** and **YourProj-Test**  
Edit Schemes to set all **Build Configurations** to corresponding **Release** or **Debug**  

## Project Folder
### Info.plist  
Check if **Bundle display name** is `$(PRODUCT_NAME)`

### Your swift or objective-c file 
```swift
#if DEBUG
    let hostServer = "https://myprojdemo.com/demotest"
#else
    let hostServer = "https://myprojdemo.com/demo"
#endif

```





