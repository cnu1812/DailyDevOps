# YAML - Yaml Ain't Markup Language.

### What is Markup language?

If you’ve ever made a note in the margin of a document, highlighted a passage in a book, or left a comment on a colleague’s Google Doc, the concept behind markup languages won’t be totally foreign to you. 

Similarly, A markup language is used by people and computers to add information to computer documents to help make their structure and content easier to understand. Most commonly used markup language is HTML.

## What is YAML?

YAML is a digestible data serialization language often used to create configuration files with any programming language.

Designed for human interaction, YAML is a strict superset of JSON, another data serialization language. But because it’s a strict superset, it can do everything that JSON can and more. One major difference is that newlines and indentation actually mean something in YAML, as opposed to JSON, which uses brackets and braces.

## Serialization

Serialization is the process of converting a data object—a combination of code and data represented within a region of data storage—into a series of bytes that saves the state of the object in an easily transmittable form. In this serialized form, the data can be delivered to another data store (such as an in-memory computing platform), application, or some other destination.
- Data serialization is the process of converting an object into a stream of bytes to more easily save or transmit it.
- In simpler words Serialising is the process of converting data structures into human readable formats such as JSON, CSV, and even text!

## Deserialization

![image](https://hazelcast.com/wp-content/uploads/2021/12/serialization-deserialization-diagram-800x318-1.png)

The reverse process—constructing a data structure or object from a series of bytes—is deserialization. The deserialization process recreates the object, thus making the data easier to read and modify as a native structure in a programming language.

### Example
- Serialized(JSON)
```
{
  "name": "Emily",
  "age": 20,
  "children": ["Roxanne", "Alexia"]
}
```
- Deserialized
```
struct Person {
    name: String,
    age: u64,
    children: Option<Vec<String>>, // Person might not have any children at all
}
```

Benifits of YAML:
- Simple and easy to read
- Nice and Strict Syntax
- Most Languages use it
- More powerful when representing complex data

<b><i> YAML is case-sensitive, spaces are important</i></b>
