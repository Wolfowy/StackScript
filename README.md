# StackHash
A "programming language" (if you can even call it a language) interpreter written in javascript inspired mostly by GolfScript and reverse polish notation :-)

To play around with the language, edit the ```code``` variable inside "index.js" file (leave \`\` as they are, edit only inside of it).

Type ```node .``` in the command line inside the folder with the files to see the output.

To see the stack output as an array, just add the ```,false``` to ```let output = interpreter(code);``` in the index.js (should look like: ```let output = interpreter(code, false);```)

## How does the language work?

Interpreter prepends every value passed to the "stack" (array). There are functional characters:

  **"I'm a string"** -> **prepends** the *"I'm a string"* string to the stack (you can make the string using the **"** character)
  
  **123.456** -> **prepends** a number to the stack (floats supported)
  
  **+** -> **adds** the first and the second value of the stack, then puts the new value onto the stack, while removing the two added ones
  
  **-** -> **subtracts** the first value from the second one from the stack, then puts the new value onto the stack, while removing the two subtracted ones
    
  **\*** -> **multiplies** the first and the second value of the stack, then puts the new value onto the stack, while removing the two multiplied ones
  
  **/** -> **divides** the second value by the first one of the stack, then puts the new value onto the stack, while removing the two divided ones
  
  **%** -> the second value **modulo** the first value of the stack, then puts the new value onto the stack, while removing the two other ones
  
### *incomplete yet*
