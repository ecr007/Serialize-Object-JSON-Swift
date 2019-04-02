# Serialize-Object-JSON-Swift

```swift
class Persona: Codable{
	private var name:String
	private var age:Int
	
	init (n:String,a:Int){
		name = n
		age = a
	}
	
	public func getName() -> String{
		return name
	}
	
	public func getAge() -> Int{
		return age
	}
}

var personas = [Persona]()

personas.append(Persona(n: "TITO Martinez", a: 29))


var strJson:Data = try JSONEncoder().encode(personas[0])

var new = try JSONDecoder().decode(Persona.self, from: strJson)

print(new.getName())
```
