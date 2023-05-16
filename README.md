# govuk-frontend-embedded

Stylesheet for embedding into webpages intended to be downloaded and saved on a user's computer

Downloaded html documents should have zero dependancies, the following changes have been made to the default `govuk-frontend` stylesheet:

* font-face for GDS Transport removed
* Crown logo in footer is embedded using base-64

A subset of the GDS components have been included that are `print safe`, meaning they do not have interactivity or rely on Javascript to function, the following have been removed:

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
