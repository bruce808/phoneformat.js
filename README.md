meteor phoneformat.js
==============

Javascript phone number formatter for meteor.

##Usage
`meteor add dispatch:phoneformat.js`

```
// Returns: +18646978257
Phoneformat.formatE164('US', '8646978257');

// Returns: US
Phoneformat.countryForE164Number('+18646978257');

// Returns: +1 (864) 697-8257
Phoneformat.formatInternational('US', '8646978257');

// Returns: (864) 697-8257
Phoneformat.formatLocal('US', '8646978257');

// Returns: United States
Phoneformat.countryCodeToName('US');

// Returns: United States
Phoneformat.dialCodeToName('+1');

// Returns: +1
Phoneformat.countryCodeToDialCode('US');

// Returns: +18646978257
Phoneformat.cleanPhone('+1 (864) 697-8257');
```

<br>

##Template
`{{> InternationalPhoneInput}}`

This provides a template for a split input field for both an international dial code and the national phone format.

```
// The value from the dial code and phone number inputs
// Ex. +15555555555
Template.InternationalPhoneInput.value();

// The dial code input value
// Ex. +1
Template.InternationalPhoneInput.dialCode();

// The phone number input value
// Ex. 5555555555
Template.InternationalPhoneInput.phoneNumber();

// Set the dial code input value
Template.InternationalPhoneInput.dialCode('+1');

// Set the phone number input value
// Ex. 5555555555
Template.InternationalPhoneInput.phoneNumber('5555555555');
```

<br>

##Credits
This repo was originally forked from [albeebe/phoneformat.js](https://github.com/albeebe/phoneformat.js).
