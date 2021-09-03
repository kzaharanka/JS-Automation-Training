# Hometask 2
## Task 1
```
function palidromTest(word) {
    let x = String(word);
    let y = '' ;
    let resultFunc = 'Not Palindrom'

    for (let i = x.length -1 ;  i >= 0  ; --i) {
     y = y + x[i]
    }

    if (x === y) {
       resultFunc = 'Palindrom'
    } 
    return resultFunc
}
let result = palidromTest('new');
console.log(result);
```
## Task 2
```
function characterChange(text, letterNumber, newText) {
    let x = String(text);
    let y = '';   
    for (let i = 0; i < x.length; i++) {
        if (i === letterNumber-1) {  
            y = y + newText
        continue
        }  
        y = y + x[i]
    }
return y
}
```
## Task 3
```
let table = {
    flag:5675,
    myPromises: [],
    element: {},
    screenshot: null,
    elementText: new String,
    allEmentsText: 'const',
    counter: 11,
    config: 'coMMon',
    const: 'FIRst',
    parameters: [1,2,3,4,5,6,7,8],
    description: 'new text'
}

let tableJson = JSON.stringify(table)

function fileTest(file){
    let x =  JSON.parse(file);
    const errorTest = {};

    if (typeof x.flag !== 'boolean') errorTest.flag = 'property is not boolean';     
    if (!Array.isArray(x.myPromises)) errorTest.myPromises = 'property is not array';
    if (typeof x.element !== 'object') errorTest.element = 'property is not object';
    if ( x.screenshot !== null) errorTest.screenshot = 'screenshot is not null';
    if (typeof x.elementText !== 'string') errorTest.elementText = 'property is not string';
    if (!x.allEmentsText.includes('const')) errorTest.allEmentsText = 'property is not contain "const" in string';
    if (x.counter <= 10) errorTest.counter = 'property is not more than 10';
    if (!x.const.includes('FIRst')) errorTest.const = 'property is not FIrst';
    if (x.config.toLowerCase() !== 'Common'.toLowerCase()) errorTest.config = 'property is not equal to Common';
    if (!x.parameters.length < 8 && x.parameters.length > 8 ) errorTest.parameters = 'array not length 8';
    if (!x.description.length < 5 && !x.description.length > 15 ) errorTest.description = 'string with length not more than 5 but less than 13 ';

const isEmpty = obj => {
    for (let key in obj) {
        return false;
      }
      return true;
}
return isEmpty(errorTest) ? console.log('OK') : console.log(JSON.stringify(errorTest))
}

let result = fileTest(tableJson);
```

