# Invoice Templates

This repository holds invoice templates made with HTML and CSS (with no JavaScript). 

The printout fits the A4 format, and the Invoice Generator project uses both. The HTML invoice can be easily printed in PDF and sent as an attachment in the email.

## How to use it

Replace all the "moustache" tags. It begins with two opening braces `{{` and ends with two closing braces `}}`.

### Header section

1. {{F1}} - issuer company name
1. {{F2}} - issuer street address
1. {{F3}} - issuer VAT number
1. {{F4}} - issuer email address
1. {{F5}} - issuer phone number

### Invoice section

1. {{F6}} - invoice number
1. {{F7}} - value date
1. {{F8}} - due date
1. {{F9}} - payment terms

### Customer section

1. {{F10}} - customer name
1. {{F11}} - customer VAT number
1. {{F12}} - customer street address

### Order section

1. {{F13}} - description
1. {{F14}} - quantity
1. {{F15}} - quantity unit
1. {{F16}} - item amount
1. {{F17}} - discount rate
1. {{F18}} - value amount
1. {{F19}} - VAT rate
1. {{F20}} - gross amount
1. {{F21}} - total amount

### Financial section

1. {{F22}} - invoice currency
1. {{F23}} - bank name
1. {{F24}} - bank SWIFT number
1. {{F25}} - bank account
1. {{F26}} - payment status
1. {{F27}} - payment method

## Invoice items

To generate many lines of ordered items, simply grab row template from the invoice template, it is between those two tags: 

```<row-template></row-template>``` 

This can be done with REGEX: 

```(?<=<row-template>)((.|\n)*)(?=<\/row-template>)``` 

Once done, replace tags `{{F13..F20}}` with your data for each item and put it back to the invoice template.

## Endnote

More language versions will be added.
