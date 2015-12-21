# aws-api-gateway-xwwwformurlencoded-2-json

This [API Gateway](https://aws.amazon.com/api-gateway/) mapping template parses
form body data (encoded as `x-www-form-urlencoded`) to JSON key-value pairs. It's handy when
your [Lambda](https://aws.amazon.com/lambda/) function needs to accept data POSTed from a HTML form.

This project is heavily influenced by the work of avilewin, whose code is
[available the AWS forums](https://forums.aws.amazon.com/thread.jspa?messageID=673012&tstart=0#673012).

# Test Cases
xwwwformurlencoded-2-json correctly parses the following types of form data strings:

- `key=value`
- `key=value&foo=bar`
- `key=`
- `key=value&foo=`
- `key=value&foo=&hello=world` (and so on)

Further, xwwwformurlencoded-2-json does the Right Thing by ignoring these malformed
form data strings:

- `=`
- `&`
- `=value`
- `key=value&`

# Author
Christian E Willman
christian@willman.io

# License
MIT
