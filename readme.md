# React Credit Card Input

> A credit/debit card input field for React

## Example

[Click here for an interactive demo](https://medipass.github.io/react-credit-card-input)

![](./example.gif)


## Install

```
$ npm install --save react-credit-card-input
```


## Usage

```js
import CreditCardInput from 'react-credit-card-input';

<CreditCardInput
  cardNumberInputProps={{ value: cardNumber, onChange: this.handleCardNumberChange }}
  cardExpiryInputProps={{ value: expiry, onChange: this.handleCardExpiryChange }}
  cardCVCInputProps={{ value: cvc, onChange: this.handleCardCVCChange }}
  fieldClassName="input"
/>
```

## Available props

<table>
<thead><tr><th>Prop</th><th>Type</th><th>Default value</th><th>Description</th></tr></thead>
<tbody>
  <tr><td>  cardNumberInputProps </td><td>object (optional)</td><td>{}</td> <td>Card number input element props<br/>(e.g. { value: cardNumber, onChange: this.handleCardNumberChange, onBlur: this.handleCardNumberBlur })</td></tr>
  <tr><td>  cardExpiryInputProps </td><td>object (optional)</td><td>{}</td> <td>Card expiry date input element props<br/>(e.g. { value: expiry, onChange: this.handleCardExpiryChange, onBlur: this.handleCardExpiryBlur })</td></tr>
  <tr><td>  cardCVCInputProps </td><td>object (optional)</td><td>{}</td> <td>Card CVC input element props<br/>(e.g. { value: cvc, onChange: this.handleCardCVCChange, onBlur: this.handleCardCVCBlur })</td></tr>
  <tr><td colspan="4"></tr>
  <tr><td>  cardImageClassName </td><td>string (optional)</td><td>''</td> <td>Class name for the card type image</td></tr>
  <tr><td>  cardImageStyle </td><td>object (optional)</td><td>{}</td> <td>Style for the card type image</td></tr>
  <tr><td>  containerClassName </td><td>string (optional)</td><td>''</td> <td>Class name for the field container</td></tr>
  <tr><td>  containerStyle </td><td>object (optional)</td><td>{}</td> <td>Style for the field container</td></tr>
  <tr><td>  dangerTextClassName </td><td>string (optional)</td><td>''</td> <td>Class name for the danger text</td></tr>
  <tr><td>  dangerTextStyle </td><td>object (optional)</td><td>{}</td> <td>Style for the danger text container</td></tr>
  <tr><td>  fieldClassName </td><td>string (optional)</td><td>''</td> <td>Class name for the field</td></tr>
  <tr><td>  fieldStyle </td><td>object (optional)</td><td>{}</td> <td>Style for the field</td></tr>
  <tr><td>  inputClassName </td><td>string (optional)</td><td>''</td> <td>Class name for the inputs</td></tr>
  <tr><td>  inputStyle </td><td>object (optional)</td><td>{}</td> <td>Style for the inputs</td></tr>
  <tr><td>  invalidClassName </td><td>string (optional)</td><td>'is-invalid'</td> <td>Class name for the invalid field</td></tr>
  <tr><td>  invalidStyle </td><td>object (optional)</td><td>{}</td> <td>Style for the invalid field</td></tr>
  <tr><td colspan="4"></tr>
  <tr><td>  inputComponent </td><td>string, function, class (optional)</td><td>'input'</td> <td>Input component for the card number, expiry and CVC input</td></tr>
</tbody>
</table>

## Integrating with form libraries

### redux-form usage

Note: this is using redux-form v6!

```js
import { Field } from 'redux-form'
import CreditCardInput from 'react-credit-card-input';

<CreditCardInput
  fieldClassName="input"
  inputComponent={Field}
  cardNumberInputProps={{ name: 'cardNumber' }}
  cardExpiryInputProps={{ name: 'expiryDate' }}
  cardCVCInputProps={{ name: 'cvc' }}
/>
```

## Contributing

Contributing to `react-credit-card-input` is easy! With four simple steps:

### Create a branch

1. Fork the repository
1. `git clone <your-repo-url>` to clone your GitHub repo to your local one
1. `git pull origin master` to pull the latest code
1. `npm install` to install the project's dependencies
1. `git checkout -b the-name-of-my-branch` to create a branch (use something short and comprehensible, such as: `fix-card-number-issue`).
1. `git remote add upstream https://github.com/medipass/react-credit-card-input.git` and `git pull upstream master` to update your fork from this source.
  
### Make the change

Note: You can run `npm run storybook`, and then navigate to http://localhost:9001/ to interactively develop your changes. If you are developing a new feature, make sure to add a story for it!

### Test the change 
1. Run `npm run fix` from the project root (This will run Prettier and ESLint and automatically fix any issues).

### Push the change!
1. `git add -A && git commit -m "My message (#issue-number/pr-number)"` (replacing `My message (#issue-number/pr-number)` with a commit message, such as `Fixed card number issue (#43)`) to stage and commit your changes
1. `git push my-fork-name the-name-of-my-branch`

## License

MIT © [Medipass Solutions](https://medipass.com.au)
