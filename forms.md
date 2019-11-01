# Forms
## Introduction
>If you want to use \<form> tag you need to respect the forms standard of Angular
### Approaches
There are two approaches/ types:
1. Template based forms
2. Reactive forms

## How to ?
### Steps
1. Import FormsModule
2. \<form> tag with inputs and `#formulaire="ngForm"`
3. Specify the controled elements with `ngModel` in the attribute
    avec un nom
4. Référencer les inputs avec # et `ngForm` type in the onSubmit method

> We need to cast the form tag using 
    `<form #formulaire="ngForm">`

Angular adds classes to **form** and **input** tags like this:
> **prestine**: The input changed before != dirty
> **valid**: The input selected != invalid
> **touched**: The input selected != untouched

> @property {boolean} untouched True if control has not lost focus yet.
@property {boolean} touched True if control has lost focus.
@property {boolean} pristine True if user has not interacted with the control yet.
@property {boolean} dirty True if user has already interacted with the control.

## Validation
### Regular expressions
We can use the website https://regexr.com/
### Directives of angular
`[email]` : on input validate email

> We can use `#email="ngModel` on the input to get the input sous forme de **ngModel**. That means we can do `email.invalid && email.touched`. We can also use `form.invalid && form.touched`

> Only put `ngModel` on inputs not buttons



