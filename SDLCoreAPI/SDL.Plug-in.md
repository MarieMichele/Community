```csharp
//create a translation provider entry and specify the path to the tm
var entry = new TranslationProviderCascadeEntry(@"path to the tm", true, true, true);
//get default project translation provider configuration
var providerConfiguration = project.GetTranslationProviderConfiguration();
//override project default settings in order to allow us to specify tm's
providerConfiguration.OverrideParent = true;
//add the translation provider to the configuration
providerConfiguration.Entries.Add(entry);
//set tm for all language pairs
project.UpdateTranslationProviderConfiguration(providerConfiguration);
```
