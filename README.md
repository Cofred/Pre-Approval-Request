# Pre-Approval-Request
Send debit approval request to User.

This API will be useful for merchant when sending Debit approval request to User for Instant Payment.

HTTP Method: POST

# Resource Url

https://cofredpayaccess.com/api/v1/PreApproval

# Headers

See our Guide for how to setup Header https://github.com/cofred/Header-Authentication

# Authentication Headers Example

merchant_id: VF9CMTY3WURPZUpJdkNnVWJWRXE=   // Base64 Encoded

secret_code: I8AtLUljNqcdS4F76OVy2Zf1bJvGwsP95rE

terminal_id: YINCU

access_token: dUp4dEtybVg0Ump4MEFT  // Base64 Encoded

timestamp: 1505628722 // Current Time in Unix Format

# Request Parameters

Field	M/O	Length	Format	Description

Account Number M	10 Numeric 	Account Number to which you want to send request

Merchant Website	M			Text		Merchant Website Url

# Note: One user can be requested once per website.

# Sending Parameters

account_number (For Account Number)
merchant_site (For Merchant site Url)

# API Response

A HTTP response code 200 is sent back for success

# Response Parameters

Field	Description

responseCode	Response Code
responseMessage Response Message
account_number Account Number
symbol Account Symbol
name Account Holder Name

# Sample Response

200

{
  "responseCode":"200",
  "responseMessage":"Pre-approval payment request was successful.",
  "account_number":"0012675778",
  "symbol":"GHS",
  "name":"Account Holder Name"
}

# Communication

Requests will be sent over the REST protocol using POST Method.
