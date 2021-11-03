# .NET-RESTful-Custom-Processing-Sample
This is a sample project to see how the custom processing works in the .NET RESTful engine. In this sample, we are removing the data from the document, so when you get the document after processing, "Data" should be an empty byte array.

## Usage
1. Clone or download this repository
2. Open the CustomProcessingSample solution in Microsoft Visual Studio
3. Build the solution
4. After building the solution navigate to the "obj/Debug" directory for the project, there you will find the "CustomProcessingSample.dll" file
5. Copy the path to the file
6. Next we will add the following to our web.config file for the RESTful engine:
```
<appSettings>
   <add key="postProcessor" value="PATH_TO_DLL\CustomProcessingSample.dll!CustomProcessingSample.CustomProcessor" />
</appSetings>
```
7. Now, start up your RESTful engine and run a report. When you get the report the "Data" will be empty

## Documentation 
https://ohana.windwardstudios.com/m/79043/l/1453279-net-restful-engine-custom-processing
