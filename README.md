# FD 2024
- Casian Marincas

# Better Align for Visual Studio Code

Better vertical alignment with/without selection in any language for any characters or words.

## Features

- Allow align code in any language
- Align code by any characters
- Smart align with or without selection
- Auto align after you type enter

## Usage

Place your cursor at where you want your code to be aligned, and use shortcut `alt + A` or invoke the `Align` command via Command Palette.


## Extension Configuration

### `betterAlign.surroundSpace`

Default value:

```json
betterAlign.surroundSpace : {
  "colon"      : [0, 1], // The first number specify how much space to add to the left, can be negative.
                         // The second number is how much space to the right, can be negative.
  "assignment" : [1, 1], // The same as above.
  "arrow"      : [1, 1], // The same as above.
  "comment"    : 2       // Special how much space to add between the trailing comment and the code.
                         // If this value is negative, it means don't align the trailing comment.
}
```

```javascript
// Orignal code
var abc = {
  hello:      1
  ,my :2//comment
  ,friend:   3      // comment
}

// "colon": [0, 1]
// "comment": 2
var abc = {
    hello : 1
  , my    : 2  // comment
  , friend: 3  // comment
}

// "colon": [1, 2]
// "comment": 4
var abc = {
    hello  :  1
  , my     :  2    // comment
  , friend :  3    // comment
}

// "colon": [-1, 3]
// "comment": 2
var abc = {
    hello:    1
  , my:       2  // comment
  , friend:   3  // comment
}

// "colon": [-1, -1]
// "comment": 2
var abc = {
     hello:1
  ,     my:2  //comment
  , friend:3  // comment
}


// Orignal code
$data = array(
    'text' => 'something',
    'here is another' => 'sample'
);

// "arrow": [1, 3]
$data = array(
    'text'            =>   'something',
    'here is another' =>   'sample'
);

```
