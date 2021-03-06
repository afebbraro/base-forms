# Base Forms for Scales

These are the base styles for creating forms.

## Requirements

Scales patterns use the [Sass CSS preprocessor](http://sass-lang.com/), you'll need either Ruby Sass or LibSass.

## Installation

* [NPM](http://npmjs.com): `npm install --save scales-base-forms`
* [Bower](http://bower.io/): `bower install --save scales-base-forms`

## Usage

Scales provides default stacked forms, forms using an unordered/ordered list, inline forms, and inline form containers with stacked label/input:

### Default stacked
```
<form>
    <label for="account">Account #<small class="form-label--additional">(Cannot Change)</small></label>
    <input class="text-input" id="account" type="num" value="123456789" readonly>

    <label for="email">Email</label>
    <input class="text-input" id="email" type="email" placeholder="Email">
    <span class="helper-text">Enter your email address</span>

    <label for="password">Password</label>
    <input class="text-input" id="password" type="password" placeholder="Password" disabled>

    <label for="gender">Gender</label>
    <select id="gender">
        <option>Female</option>
        <option>Male</option>
        <option>Other</option>
    </select>

    <label>Introduce yourself</label>
    <textarea></textarea>

    <label for="newsletter">
        <input id="newsletter" type="checkbox"> Send me the newsletter
    </label>

    <button type="submit" class="btn">Sign in</button>
</form>
```

### Using a list
```
<form>
    <ul class="form-list">
        <li class="input-container">
            <label for="account">Account #<small class="form-label--additional">(Cannot Change)</small></label>
            <input class="text-input" id="account" type="num" value="123456789" readonly>
        </li>
        <li class="input-container">
            <label for="email">Email</label>
            <input class="text-input" id="email" type="email" placeholder="Email">
        </li>
        <li class="input-container">
            <label for="password">Password</label>
            <input class="text-input" id="password" type="password" placeholder="Password" disabled>
        </li>
        <li class="input-container">
            <label for="gender">Gender</label>
            <select id="gender">
                <option>Female</option>
                <option>Male</option>
                <option>Other</option>
            </select>
        </li>
        <li class="input-container">
            <label>Introduce yourself</label>
            <textarea></textarea>
        </li>
        <li class="input-container">
            <label for="newsletter">
                <input id="newsletter" type="checkbox"> Send me the newsletter
            </label>
        </li>
    </ul>
    <button type="submit" class="btn">Sign in</button>
</form>
```

### Inline
```
<form class="form-inline">
    <label for="account">Account #<small class="form-label--additional">(Cannot Change)</small></label>
    <input class="text-input" id="account" type="num" value="123456789" readonly>

    <label for="email">Email</label>
    <input class="text-input" id="email" type="email" placeholder="Email">
    <span class="helper-text">Enter your email address</span>

    <label for="password">Password</label>
    <input class="text-input" id="password" type="password" placeholder="Password" disabled>

    <label for="gender">Gender</label>
    <select id="gender">
        <option>Female</option>
        <option>Male</option>
        <option>Other</option>
    </select>

    <label>Introduce yourself</label>
    <textarea></textarea>

    <label for="newsletter">
        <input id="newsletter" type="checkbox"> Send me the newsletter
    </label>

    <button type="submit" class="btn">Sign in</button>
</form>
```

### Inline input containers with stacked label/input
```
<form>
    <ul class="form-list">
        <li class="input-container input-container--inline">
            <label for="account">Account #<small class="form-label--additional">(Cannot Change)</small></label>
            <input class="text-input" id="account" type="num" value="123456789" readonly>
        </li>
        <li class="input-container input-container--inline">
            <label for="email">Email</label>
            <input class="text-input" id="email" type="email" placeholder="Email">
        </li>
        <li class="input-container input-container--inline">
            <label for="password">Password</label>
            <input class="text-input" id="password" type="password" placeholder="Password" disabled>
        </li>
        <li class="input-container input-container--inline">
            <label for="gender">Gender</label>
            <select id="gender">
                <option>Female</option>
                <option>Male</option>
                <option>Other</option>
            </select>
        </li>
        <li class="input-container input-container--inline">
            <label>Introduce yourself</label>
            <textarea></textarea>
        </li>
        <li class="input-container input-container--inline">
            <label for="newsletter">
                <input id="newsletter" type="checkbox"> Send me the newsletter
            </label>
        </li>
        <li class="input-container input-container--inline">
            <button type="submit" class="btn">Sign in</button>
        </li>
    </ul>
</form>
```

## Available Classes

* `.form-list`
* `.input-container`
* `.input-container--inline`
* `.form-label`
* `.form-label--additional`
* `.text-input`
* `.form-inline`
* `.is-disabled`
* `.is-readonly`
* `.helper-text`

## Available Variables

* `$fieldset-padding`
* `$text-input-padding`
* `$text-input-border-width`
* `$text-input-border-style`
* `$text-input-border-color`
* `$text-input-border-radius`
* `$input-container-margin-bottom`
* `$input-container-inline-valign`
* `$input-disabled-border-color`
* `$input-disabled-background-color`
* `$input-disabled-text-color`
* `$input-readonly-border-color`
* `$input-readonly-background-color`
* `$input-readonly-text-color`
* `$helper-text-hidden` - change from `true` to be visible by default

### The Scales Namespace Variable

All Scales patterns expose the `$scales-namespace` variable.

`$scales-namespace` accepts a string that will prefix all Scales classes. The default value is `null`.

To give all Scales classes a namespace, you will need to set this variable in a file that is imported before any scales files. For example:

```
@import your-project/settings; // $scales-namespace is set in this file
@import your-project/scales; // Imports the Scales library
@import your-project/project // The rest of your project imports
```
