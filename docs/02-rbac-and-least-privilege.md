# Lab 02 - Role-Based Access Control (RBAC) and Least Privilege

## Objective

Demonstrate how Azure RBAC can be used to enforce least-privilege access while identifying and correcting excessive permissions.

## Environment

- Microsoft Azure
- Microsoft Entra ID (Azure AD)
- Azure Storage Account
- Resource Groups
- Azure Activity Logs

## Scenario

Three users were created to represent different business functions:

| User | Role |
|--------|--------|
| Kwame | Developer |
| Yahaya | Analyst |
| Aliya | Technical Support |

The goal was to assign only the permissions required for each role.

## Activities Performed

### Developer Access

Assigned the Storage Account Contributor role at the Resource Group level.

Permissions:

- Create storage resources
- Modify storage resources
- Manage storage configurations

### Analyst Access

Initially assigned Storage Blob Data Contributor at the Subscription level.

This created an excessive permission condition because the user could:

- Upload files
- Modify files
- Delete files
- Access storage across the subscription

### Technical Support Access

Assigned Support Request Contributor.

Permissions:

- Open support requests
- View resource status

No access was granted to modify resources.

## Misconfiguration Identified

The Analyst account was over-permissioned.

Risk:

- Excessive access violated the Principle of Least Privilege.
- Data deletion or modification could occur across multiple storage resources.

## Remediation

Removed the Storage Blob Data Contributor role.

Assigned:

Storage Blob Data Reader

Scope:

Specific container only.

Result:

- Read-only access
- No upload permissions
- No delete permissions
- Reduced attack surface

## Audit Validation

Azure Activity Logs were reviewed to verify:

- Role assignment events
- Role removal events
- Administrative actions

## Security Concepts Demonstrated

- Least Privilege
- Role-Based Access Control (RBAC)
- Access Governance
- Identity Security
- Audit Logging
- Separation of Duties

## Evidence

Screenshots will be stored in:

docs/screenshots/