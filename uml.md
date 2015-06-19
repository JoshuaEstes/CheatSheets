UML Cheat Sheet
===============


```
<<interface>>
<<abstract>>
<<concrete>>

- private
# protected
+ public

name : type = default value
```

Examples:

```
<<abstract>>
Name\Space\To\ClassAbstract
---
- $privateAttribute : string = ''
# $protected : integer = 1
+ $public : string = 'DefaultValue'
---
+ getPrivateAttribute() : string
+ getValueForKey($key : string) : mixed
+ get($key : string, $default : mixed = null) : mixed
```

```
Class A "uses" Class B
[Class A]- - - ->[Class B]
```

```
Class A "has a" Class B
[Class A]---->[Class B]
```

```
Company "owns" Employee
[Company]⃟----[Employee]
```

```
Ford "is a" Car
[Car]◁----[Ford]
```
