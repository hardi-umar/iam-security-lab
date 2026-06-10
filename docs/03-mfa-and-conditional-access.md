# Lab 03 - Multi-Factor Authentication (MFA) and Conditional Access

## Objective

Demonstrate how Microsoft Entra ID can strengthen authentication security through Multi-Factor Authentication (MFA) and Conditional Access policies.

## Environment

- Microsoft Entra ID
- Microsoft Authenticator
- Conditional Access Policies
- Azure Sign-In Logs

## Scenario

An organization wants to reduce the risk of credential compromise by requiring additional verification before granting access to cloud resources.

## Activities Performed

### MFA Deployment

Configured MFA requirements for user accounts.

Authentication methods:

- Microsoft Authenticator
- Push Notification
- Number Matching

### Conditional Access Policy

Created a policy requiring MFA when:

- Access originates from an unknown location
- Access originates from unmanaged devices
- Administrative accounts authenticate

### Authentication Testing

Validated:

- Successful MFA enrollment
- Successful MFA challenge
- Successful sign-in after verification
- Blocked access when policy requirements were not met

## Security Benefits

- Reduces credential theft risk
- Protects against password spraying
- Protects against phishing attacks
- Strengthens identity verification

## Security Concepts Demonstrated

- Multi-Factor Authentication
- Conditional Access
- Identity Protection
- Authentication Security
- Zero Trust Principles

## Evidence

Screenshots will be stored in:

docs/screenshots/