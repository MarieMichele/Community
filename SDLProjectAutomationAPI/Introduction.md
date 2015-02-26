```csharp
IExtensionPoint extensionPoint = PluginManager.DefaultPluginRegistry.GetExtensionPoint<FileTypeComponentBuilderAttribute>();
foreach (IExtension extension in extensionPoint.Extensions)
{
    IFileTypeComponentBuilder extensionFileTypeComponentBuilder = (IFileTypeComponentBuilder) extension.CreateInstance();
    extensionFileTypeComponentBuilder.FileTypeManager = fileTypeManager;
    IFileTypeInformation extensionFileTypeInformation = extensionFileTypeComponentBuilder.BuildFileTypeInformation(string.Empty);
    string extensionFileTypeDefinitionId = extensionFileTypeInformation.FileTypeDefinitionId.Id;
     FileTypeComponentBuilderAttribute attr = extension.ExtensionAttribute as FileTypeComponentBuilderAttribute;
    if (Equals(extensionFileTypeDefinitionId, "XML v 1.2.0.0") && attr.IsTemplate)
    {
        //Do something with the file type component builder
    }
}
```
