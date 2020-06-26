# Generate and install self signed certificates

## Generate

#### Generate `local.crt` and `local.key` files

`openssl req -x509 -nodes -days 3650 -newkey rsa:2048 -keyout local.key -out local.crt -config local.cnf`

## Installation

Install the `local.crt` on your machine

### Windows instructions

1. Open `local.crt`
2. Click "Install Certificate..."
3. Choose either "Current User" or "Local Machine"
4. Choose "Place all certificate in the following store"
5. "Browse..." to "Trusted Root Certification Authority"
6. Click "Next", "Finish" and finally "OK"

This will install the generated certificate on your local machine and will be trusted by all the software, including the browsers.