# @womorg/studious-telegram

Adds ability to:
- read clipboard's content
- write to clipboard


<h2>Notice</h2>
<p>Since it uses Chrome Devtools Protocol,</p>
<p>This package works with Chrome.</p>
- Electron is not supported.

<br />
<h2>Install</h2>
<br />

```
npm install @womorg/studious-telegram;
```

<h3>Or</h3>

```
yarn add @womorg/studious-telegram
```

<h2>Usage</h2>
<br />
<h3>Copy string to clipboard</h3>
<br />


```
import '@womorg/studious-telegram';

cy.get('SOME SELECTOR')
    .invoke('text')
    .copyToClipboard(); 
```

<h3>Or</h3>

```
import '@womorg/studious-telegram';

cy.wrap('SOME STRING VALUE')
    .copyToClipboard(); 
```

<br />
<h3>Copy from clipboard</h3>
<br />

```
import '@womorg/studious-telegram';
cy.copyFromClipboard().then(clipboardData => {})

```

<h3>Or</h3>

```
import '@womorg/studious-telegram';
cy.copyFromClipboard().should('eq', 'EXPECTED VALUE');

```

<br />


<h3>Special thanks to </h3>
Gleb Bahmutov
For <a href="https://www.npmjs.com/package/cypress-cdp" target="_blank">cypress-cdp</a> package, 
and for <a href="https://www.youtube.com/watch?v=4eEc3x24D64">this amazing youtube video</a> about adding permissions to Cypress.
It helped me alot.

