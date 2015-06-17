Just a sample contribution for testing

```csharp
public override SearchResults[] SearchTranslationUnitsMasked(SearchSettings settings, TranslationUnit[] translationUnits, bool[] mask)
{
  var results = base.SearchTranslationUnitsMasked(settings, translationUnits, mask);
  //iterate thru results and take the translation units which have context now
  return results;
}
```
