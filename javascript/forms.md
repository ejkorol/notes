# HTML Forms

## What the heck are they?

They are a collection of various input fields that allow a website to collect user information via the `<form>` element.

*`<form>` does not have any appearance, it is instead used as a wrapper.*

```
<form action="URL" method="POST">
    <!-- Form Elements -->
</form>
```
> This is a basic form!

> ## All proceeding inputs, fields and selectors will be wrapped within this element.

## Fields

There are multiple fields we can leverage to collect user information and have that processed as a certain data type.

### Input

```
<input type="text">
<input type="email">
```
> Used to collect key value pairs that a server can later access.

### Textarea

```
<textarea name="<something>">
</textarea>
```
> Used like a 'text' type input, but for multi-line text.

### Selectors

#### Radio

```
<input type="radio">
```
> Radios are useful to make a single selection.

#### Checkbox

```
<input type="checkbox">
```
> Useful to make multiple selections.

#### Selections

```
<select name="">
    <option value="">
    <option value="">
</select>
```
> Useful to force a user for a selection from predefined options.

## Submit The Form

There are multiple ways to submit a form:
You may notice that for all submit methods, there is a type of `submit` required to execute the submit method itself.

### Buttons

```
<button type="submit"></button>
```
> This is a newer, and nicer way.

### Input

```
<input type="submit">
```
> While this is an older way of handling a submit, it is still present in legacy sites.

### Input Types

Here are all the `types` available in input:

```
<input type="button">
<input type="checkbox">
<input type="color">
<input type="date">
<input type="datetime-local">
<input type="email">
<input type="file">
<input type="hidden">
<input type="image">
<input type="month">
<input type="number">
<input type="password">
<input type="radio">
<input type="range">
<input type="reset">
<input type="search">
<input type="submit">
<input type="tel">
<input type="text">
<input type="time">
<input type="url">
<input type="week">
```

## Hidden Fields

Hidden fields can be used to pass data that is not relative to the user input itself.
They wont be displayed in the browser, but are seen in the source code.

```
<input type="hidden" name="" value="">
```
> These aren't so commonly used.

## Labels

Labels are used to give context to forms, and are a necessary to accessbility.
Moreover, they are essential to connect an input element using a `for` attribute.

- *The `for` attribute must match the `id` of the input element.*
- *Clicking the label will focus the input*

## Form Events

```
const form = document.getElementById('myForm');
form.addEventListener('submit', (e) => {
    e.preventDefault();
    console.log('Form Submitted');
});
```
> This is how we can listen to form submissions with javascript.

In this example we are referencing a `const` called form by getting that element via it's `id`, then we are adding an event listener to it, and listening for the `submit` event.

### Accessing Form Values

```
const form = document.getElementById('myForm');
form.addEventListener('submit', (e) => {
    e.preventDefault();
    console.log(e.garget.petPref.value);
    console.log(e.garget.cities.value);
});
```

Where `e.target.<input name>.value` is the `name` attribute of the targetted `input` and `value` is the assigned `value` attribute on the `input`.

```
<input type="radio" name="petPref" value="dogs" />
```

## Validation

Validation is the process of checking whether the user has inputed the correct information that you require to submit a form.

For example, for the `email` type, you most likely want a properly formatted email including the '@' symbol:

```
const email = document.getElementById('mail');
const message = document.getElementById('message');

email.addEventListener('input', (e) => {
    if (!email.value.includes('@')) {
        message.innerText = 'please enter a valid email'
    }
});
```
