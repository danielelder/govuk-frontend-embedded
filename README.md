# govuk-frontend-embedded

This is a proof of concept for creating stylesheets that can be embeded into webpages so they can be downloaded and saved on a user's computer.

> Current govuk-frontend version: **4.6.0**

Downloaded html documents should have zero dependancies, the following changes have been made to the default `govuk-frontend` stylesheet:

* font-face for GDS Transport removed
* Crown logo in footer is embedded using base-64

## Options

There are 2 versions of the CSS, a colour version and a black and white version.

### Colour version

This is a like-for-like version of the govuk-frontend styles created as a standalone file.

### Black and white version

The black and white version is the colour css file with some overrides to make it render the same as the printed output. 

## Supported components

A subset of the GDS components have been included that are `print safe`, meaning they do not have interactivity or rely on Javascript to function:

* details
* footer
* header
* inset-text
* notification-banner
* panel
* phase-banner
* tag
* skip-link
* summary-list
* table
* warning-text

The following component styles have been removed:

* Accordion
* Back link
* Breadcrumbs
* Cookie banner
* Error message
* Error summary
* Details
* Pagination
* Tabs
* All form controls

The following components have been modified to remove interactivity but are still usable if required

* Summary list actions

## How to use

1. Create a bare bones html file, for example:

```html
<!DOCTYPE html>
<html lang="en" class="govuk-template">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document title - HMRC - GOV.UK</title>
</head>
<body class="govuk-template__body">
    
</body>
</html>
```

2. Add an empty set of `<style>` tags just before the closing `<head>` element:

```html
<head>
    ...
    <style>

    </style>
</head>
```

3. Paste in the contents of the `css/embed-colour.css` or `css/embed-black-and-white.css`.

4. Create your page - Add a header, footer and any required content. 

To test just open the file in the browser, no server required.

## Production use

This project only serves as an example of how to implement embedded css into a webpage page.

Projects should implement there own solution and not rely on this repo being kept up to date.
