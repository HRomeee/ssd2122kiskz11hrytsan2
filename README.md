# ssd2122kiskz11hrytsan2
For current project you need to install next packages:

Install-Package ini-parser

Install-Package Newtonsoft.Json -Version 13.0.1

For this you can write string above at PM package console (https://www.nuget.org/packages/Newtonsoft.Json, https://github.com/rickyah/ini-parser).
Also for work with .xml extention you need to add references to next packages:

System.Xml

System.Xml.Linq

System.Xml.Serializations

For thit you can add references at project by context menu and choose 'Assemblies' filter.
All those packages needed for correct work with supported extentions (.ini, .json, .xml).

If you want to use files created by yourself, all those files should have next structure:
.ini:

Sequence variable should be inside 'DataModel' block. If .ini file contains another data, it will be ignored.

Example:
```ini
[DataModel]
Sequence = (n*2+2/n*(1+5))/2
```

.Json:

Sequence variable should be inside curve brackets, as at default json format.

Example:
```json
{"Sequence":"(n*2+2/n*(1+5))/2"}
```
.xml:

Sequence variable should be inside 'DataModel' tag. If .xml file contains another data, it will be ignored.

Example:
```xml
<?xml version="1.0"?>
<DataModel xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <Sequence>(n*2+2/n*(1+5))/2</Sequence>
</DataModel>
```
