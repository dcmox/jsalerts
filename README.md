# jsalerts
JSAlerts is a simple replacement for DOM popups. Include the provided JS file and replace the alert(), confirm(), and prompt() interfaces.

![JSAlerts](https://i.imgur.com/NgPG8EC.jpg)

## Use
This package/script replace the default alert(), confirm(), and prompt() interfaces. Instead of using the format:

```js
if (confirm("Confirm message here")) {
    // perform action
}
```

You provide a callback instead, such as:

```js
    const onConfirm = () => {
        // perform action onConfirm
    }
    const onCancel = () => {
        // perform action onCancel
    }

    const onConfirmPrompt = (value) => {
        console.log(value) // value provided by input
    }

    // For confirmation
    document.getElementById('confirmButton') = () => {
        confirm('Are you sure you want to proceed?', 'Title', onConfirm, onCancel)
    }

    // For prompts
    document.getElementById('promptButton') = () => {
        prompt('Question goes here', 'Default answer', onConfirmPrompt)
    }

    // Standard alert
    alert('Message', 'Title', optionalOnConfirm)
```

## Customization
You can customize the style of JSAlerts via the jsalerts.css file.

## Todo 
* Add support for popup(`html goes here`, width, height) to allow custom HTML popups.
