# YAML
## What is YAML?
* YAML(YAML Ain't Markup Language) is a human-readable data serialization format.
* It is commonly used for configuration files and data exchange between systems.
* YAML is desinged to be easy to read and write, making it popular amoung developers and system administrators.
## Syntax
YAML used indentation and colons to structure data.
Here's an example of YAML system:
```yaml
key: value
nested_key:
  - item1
  - item2
```
* YAML uses indentation to indicate the nesting of elements.
* Spaces are recommended over tabs, and number of spaces for indentation conventionally, two spaces are used for indentation.
## Comments
Comments in YAML start with **#** character and are used to provide explainatory or descriptive text.
* Comments are ignored by the YAML parser.
```yaml
# This is a comment
key: value  # This is another comment
```
## DataSturctures
## Scalars
* Scalar represent simple values like strings, numbers, booleans and null.
* Scalar don't have any indentation and can be expressed directly.
```yaml
string_key: Hello, world!
number_key: 42
boolean_key: true
null_key: null
```
## Lists
* Lists are represented by using a hyphen(-) followed by a space.
* Lists can contain any combination of scalars, other lists, or mappings(key-value pairs)
* If one key has multiple values, then lists are used.
```yaml
list_key:
  - item1
  - item2
  - sub_list:
    - sub_item1
    - sub_item2
```
## Mappings
* Mappings represent key-value pairs and use a colon(:) to separate the key from the value.
* Mappings can be nested with each other.
```yaml
person:
  name: John Doe
  age: 30
```
## Multiline Scalars
If a scalar value spans multiple lines, you can use the **|(pipe)** character to indicate a literal block scalar or **>** character to indicate a folded scalar.
```yaml
multiline_key: |
  This is a 
  multiline
  scalar value
```
## YAML validator
YAML Lint website is used to validate the YAML syntax.

[www.yamllint.com](https://www.yamllint.com/)
## --- (Triple dash)
If there are multiple YAML data in a single file, **---** represents the beginning of YAML.
## Example
```yaml
--- # Beginning of YAML
#Scalars
name: Naveen
location: Bengaluru
profession: IT
#Lists
hobbies:
  - Reading
  - Coding
  - Exploring Tech
#Mappings
favoriteFoods:
  fruits: apple
  drinks: Orange juice
#MultilineScalars
whatIsThisVideoAbout: |
  this video discuss about
  YAML syntax in detail
```