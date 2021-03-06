# C++ CODING STANDARDS

Our ethos consists of the idea that we're writing code for other people. This means we want our code to look tidy, professional, and function; to achieve this, we've had to implement some standards - which we could greatly appreciate a following to when submitting Pull Requests and the likes.

## NAMING
Consistency is key - the key to easy, readable code - especially since our code is not only for us. Naming consistency will help identify different types of variables, constants, files, methods, and more. Consistency - however - is not the final stop... Something needs to be named as per it's functionality or it's use; it should be self-explanatory, you shouldn't have to ask to understand what it is.

### FILE NAMING
All files must follow the `PascalCase` convention, where each “word” in the file name has a capital on its first letter and no spaces. All C++ files must use either `.cpp` or `.hpp` for source and header files respectively.
For example, this type of convention must be followed:

```
PascalCaseFileName.hpp
PascalCaseFileName.cpp
IWindow.hpp
IWindow.cpp
```

### CLASSES
Classes must also follow the `PascalCase` naming convention, to allow for faster reading, and identification of classes within code. For example:

```cpp
class FooBar
class Caterpillar
```
### FUNCTIONS
Functions should follow the `camelCase` convention, where the first word has a lowercase first letter, but all consequent words start with a capital letter, like so:

```cpp
int doSomething();
int goddIsTodd();
int wowThisIsACoolFunction(); 
```
### VARIABLES
There are a few things to know about naming variables. Most all variables must follow the camelCase convention, however, private member variables of a class must use an `m_` prefix before them. However, constants and macros should be ALL_CAPITALS_USING_UNDERSCORES_INSTEAD_OF_SPACES. Hopefully that makes sense, if not, here’s an example to make things make sense:

```cpp
const int THIS_IS_A_CONSTANT = 10;
int g_globalVariableForFooQuality = 5; // Global variable, uses the g_ prefix

class FooBar
{
public:
    int doThing(std::string descriptionOfThing); // Parameters also use camelCase.
    float randomNumber; // This is a normal public variable, uses no prefix.
private:
    int m_fooQuality; // This is a private member variable, uses the m_ prefix.
};
```

Do not use any hungarian notation, as we internally have found that redundant, and truly a divergence from our goal to become super saiyan.
## MISC. NAMING
Namespaces must start with lowercase characters, however, whenever creating another namespace, consult the core developer first, as overuse of namespaces can become triggering.
## COMMENTING
For any comment that requires only a single line, use the // method of commenting. Always make sure the // has a space before the actual comment. This is for easier readability, and no sudden fear to visit the opticians because we just became blind old grannies. For example:

```cpp
// This is a single line comment
int bar();
```
Multiline comments should use the /* */ method of commenting, where the /* and */ are on their own lines. Each line in between should house an asterisk, please ensure there is a space before following comment. For example:
```cpp
/*
 * This is a multiline comment
 * As in a comment with multiple lines.
 * Etc...
 */
```
When documenting classes, methods and similar we follow the Doxygen Javadoc syntax. For example, this convention should be followed:
```cpp
/**
 * @brief This class is for documentation reasons. 
 */
class FooBar {
public:
	/**
	 * @brief This does an important thing
	 * @param desc A description of the thing
	 * @return A very important integer. (probably an error code or something)
	 */
  	int doThing(std::string desc);
  	
  	float randomNumber; //< This is a single line description for a member

      /// @brief This member variable requires a longer single line comment. (filling space)
      bool foobarred;
};
```
Multiline Doxygen comments should start with a /** and end with a normal */. The second asterisk is something that Doxygen recogises through its own interpreter. There are two ways for single line comments, choose whichever one looks right, a slightly longer one however should use the second method, just so we don’t have to become grannies to read.
## MODULARISATION
Currently the code is separated by function, eg all the code for rendering is in one spot. Each module should sport a easy-to-use public API. This API should be as generic as possible in order to make the replacing, and use of code easier.
## TODO: FORMATTING, USAGE OF C++ FEATURES
