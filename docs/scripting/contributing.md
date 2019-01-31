# Contributing

When changing **Moona** code comunication is key. **ALLWAYS** talk to Maris first. This is especially important when making changes to the API.

## General Rules

## Naming

- naming should be done in **CamelCaseFashion**
- Class-names must be uppercase `public class Value { }`
- Method-names must be uppercase `private void DoStuff() { }`
- Public properties and fields must be uppercase `public int Count = 5;`
- private member variables must be lowercase and be preceded a underscore `private float _parameter = 1.0f;`
- local variables and method parameters must be lowercase

## Style

- avoid anything `static` if possible
- avoid C# properties unless you:
	- have to run code when setting a value
	- use it to controll access ie: `public T PropertyName { get; private set; }`
- access to fields and properties must be defined explicitly via `public`, `private`, `protected` or `internal`
	- in general fields should be as restrictive as possible
- classes should be defined as `sealed` where possible
- `if` statements should use `statement == false` instead of `!statement` notation
- It is preferred to have an empty line after closing curly brackets when not followed by another curly brackets or a comment.
- `if` statements as well as `for` and `while` loops should have a body wrapped in curly `{ }` braces
- Comments that explain the workings and flow of code are welcome but shouldn't be overwhelming. Use with taste.
- XML documentation comments for classes, Fields, Properties and Methods are very welcome:
```
	/// <summary>
	///
	/// </summary>
```
## Unity Specifics

- Garbage creation should be avoided
- Project specific extensions to Moona should reside in the `Assets/Moona/MoonaExtension/` folder