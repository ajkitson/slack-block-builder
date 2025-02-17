# Date Picker

?> **Note:** This document is a reference to the `DatePickerBuilder` object in **Block Builder**. For more information on how this carries over to the Slack API, view the [the Date Picker docs](https:&#x2F;&#x2F;api.slack.com&#x2F;reference&#x2F;block-kit&#x2F;block-elements#datepicker) on Slack's doc site.

### Creating an Instance 

The function that creates a new instance of `DatePickerBuilder` is available as both a top-level import and as a member of its 'category', `Elements`:

```javascript
import { DatePicker } from 'slack-block-builder';

const myObj = DatePicker(params?);

```

```javascript
import { Elements } from 'slack-block-builder';

const myObj = Elements.DatePicker(params?);
```

### Params

Each instance of the `DatePickerBuilder` object has chainable setter methods for the object's properties. However, properties with primitive values can optionally be passed to the instantiating function, should you prefer:

`actionId` – *String*

`initialDate` – *Date*

`placeholder` – *String*


?> **Note:** For an explanation of any one of the parameters, see its corresponding setter method below.

### Setter Methods

All setter methods return `this`, the instance of `DatePickerBuilder` on which it is called.

```javascript
DatePickerBuilder.actionId(string);
```

Sets a string to be an identifier for the action taken by the user. It is sent back to your app in the interaction payload when the element is interacted or when the view is submitted. 
```javascript
DatePickerBuilder.confirm(ConfirmationDialog);
```

For confirmation dialogs, sets the text of the button that confirms the action to which the confirmation dialog has been added. For elements, adds a confirmation dialog that is displayed when the user interacts with the element to confirm the selection or action. 
```javascript
DatePickerBuilder.initialDate(Date);
```

Pre-populates the date picker with a selected, default date. 
```javascript
DatePickerBuilder.placeholder(string);
```

Defines the text displayed as a placeholder in the empty input element. 

### Other Methods

The `DatePickerBuilder` object also has other methods available:

```javascript
DatePickerBuilder.end();
```

Performs no alterations to the object on which it is called. It is meant to simulate a closing HTML tag for those who prefer to have an explicit end declared for an object. 
