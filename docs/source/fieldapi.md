# Javascript Form Field API

Using javascript, you can communicate with a Blitzen form using the [window.postMessage](https://developer.mozilla.org/en-US/docs/Web/API/Window/postMessage) method.

The primary use-case for using this API is to dynamically change field values based on user interactions or events on your own website or application. In many situations, you may want to use a [query parameter](http://help.blitzen.com/article/94-how-to-use-query-parameters) in order to pre-populate a form field. This works well unless you want the ability to change the query parameter on the fly. Attempting to use dynamic query parameters will result in the form reloading which can be undesireable for a number of reasons. In order to alleviate the issues that come with pseudo-dynamic query parameters, we provide a postMessage method to provide a much cleaner implementation.

## Usage:

find the iframe element:

`var el = var el = document.getElementById("e15fe69d2b41a3932a37508ec3ba96");`
Where `getElementById` is referencing the id of the iframe element

Send a message to populate the form field:
`el.contentWindow.postMessage({'fieldId':'48891e6075903a85af0e9c506f8810', 'fieldValue':'hello world!'}, '*');`
Where `fieldId` is the `field-id` property on the DOM input element of the field you want to populate, and `fieldValue` is the string you want to enter.

## Form Field Rules

Form field rules will be updated as soon as the postMessage is successfully fired.

## Limitations

Currently this feature is only intended to be used with string fields (single line text, paragraph, email, website, etc.).

Warnings will be supplied if you have provided the wrong `fieldId` or if the `fieldValue` is blank.
