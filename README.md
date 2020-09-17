# Subscription Renewal Kata

## Goal

You just got a new job at a magazine. The CEO tells you that they're losing a lot of business, and they're pretty sure it's because people aren't checking their mailboxes for renewal forms anymore.
His solution? Use email instead! He asks you to write a program that will email subscribers that are within three months of their subscription expiring with the message "Please renew your subscription to Ferret Fancy!"

## Instructions
Design a solution that leverages the concept of Logical Core, Collaborative Shell to successfully notify these customers that they need to renew their subscriptions. The two APIs that you will interact with are provided below. Maintain a proper separation in your design so that the logic can be tested with unit tests, and API collaboration can be tested with integration tests. Use the WireMock library to stand-in for the APIs during your integration tests.

## APIs

### Retrieve Subscribers
**URL**: `http://example.domain/subscribers`

**Method**: `GET`

**Example Results**
```json
[
  { "name": "", "email": "", "expirationDate":  "2050-01-15" },
  { "name": "", "email": "", "expirationDate":  "2050-03-27" }
]
```

### Send Email

**URL**: `http://example.domain/mail`

**Method**: `POST`

**Example Results**
```json
{
  "subject": "An Important Message from Ferret Fancy",
  "body": "Please renew your subscription to Ferret Fancy!", 
  "to": ["someone@email.com", "thatone@domain.com"], 
  "from": "sales@ferretfancy.com"
}
```
