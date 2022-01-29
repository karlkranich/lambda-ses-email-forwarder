# lambda-ses-email-forwarder
This is an adaptation of the python lambda code found at https://aws.amazon.com/blogs/messaging-and-targeting/forward-incoming-email-to-an-external-destination/.  It is used in a Lambda function that is called by SES and forwards emails to a specified destination address.

The difference is that this function included the body of the forwarded email in the body of the new email, instead of attaching it as a .eml file.

All of the setup instructions on that page still apply.

This code also has a limitation of the original code: email is expected at a single pre-defined email address and forwarded to a single address (see "To Do" below).

### To Do:
- Add the ability to accept email for multiple addresses and forward each to a defined destination
