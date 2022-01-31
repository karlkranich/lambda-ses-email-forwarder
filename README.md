# lambda-ses-email-forwarder

This is an adaptation of the python lambda code found at https://aws.amazon.com/blogs/messaging-and-targeting/forward-incoming-email-to-an-external-destination/. It is used in a Lambda function that is called by SES and forwards emails to specified destination addresses.

There are two primary differences:

1. This function includes the body of the forwarded email in the body of the new email, instead of attaching it as a .eml file.
2. This function takes a list of From: and To: addresses, rather than forwarding all email to a single destination.

All of the setup instructions on that page still apply except for the way that recipients are specified (see below).

## Changelog

1/30/2022 - The function now takes an environment variable called MailAddressMap that should contain a string representing a json list of From: and To: email addresses. For example: '[{"From":"address@example.com","To":"newaddress@gmail.com"},{"From":"address2@example.com","To":"newaddress2@gmail.com"}]'

The environment variable MailRecipient is no longer used.
