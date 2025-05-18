hadoop ecosystem component
- hdfs
- mapreduce
- yarn
- hive
- pig
- hbase
- zookeeper

hadoop 2.0
- namenode duo
- hadoop federation
- map reduce 2 (mrv2)
- yarn
	- resource manager
	- node manager
	- application master

shedulers
- fair 
- capacity



mongo db

```javascript

// write
db.students.insertOne({ name: "Harsh", age: 22, course: "CSE" })

db.students.insertMany([
  { name: "Alice", age: 20 },
  { name: "Bob", age: 21 }
])

// read
db.students.findOne({ name: "Harsh" })

db.students.find({ age: { $gt: 20 } })

// update
db.students.updateOne(
  { name: "Harsh" },
  { $set: { age: 23 } }
)

db.students.updateMany(
  {},
  { $inc: { age: 1 } }
)

// delete
db.students.deleteOne({ name: "Harsh" })

db.students.deleteMany({ age: { $gt: 25 } })

```



```scala
object HelloWorld {
  def main(args: Array[String]): Unit = {
    println("Hello, World!")
  }
}

val x = 10        // Immutable (like final in Java)
var y = 20        // Mutable

def add(a: Int, b: Int): Int = a + b

class Person(val name: String, val age: Int) {
  def greet(): String = s"Hello, I’m $name"
}

val p = new Person("Harsh", 22)
println(p.greet())

case class User(name: String, age: Int)
val u1 = User("Alice", 25)

```