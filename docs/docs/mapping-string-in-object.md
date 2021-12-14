---
sidebar_position: 3
---

# Read an String

## Mapping object in string

To configure an object, you should use ` ObjectMapper ` and ` ReadProperty ` properties to map string layout.

```csharp
  [ObjectMapper(lenght: 50)]
  public class NothingReader
  {
    [ReadProperty(start:1, lenght: 19 )]        
    public string Name { get; private set; }

    [ReadProperty(start: 20, lenght: 30)]        
    public string Adress { get; private set; }
  }
```

## Instanciate

To map you object as string, you need instantiate ``` Spinner ``` passing the object type in T.

```csharp
  Spinner<NothingReader> spinnerReader = new Spinner<NothingReader>();
```

## Read Object

After configured the object, you need call the ` ReadFromString ` method to read string and convert it to object.

```csharp
  var obj = spinnerReader.ReadFromString("             spinner            www.spinner.com.br");
```