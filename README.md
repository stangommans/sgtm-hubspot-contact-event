# HubSpot Contact & Behavioral Event Tag (Server-Side)

This Google Tag Manager server-side template allows you to seamlessly integrate with HubSpot by performing two actions in a single trigger:
1. **Create or Update a Contact**: Checks if a contact exists by email. If they do, it updates their properties; if not, it creates a new record.
2. **Track Custom Behavioral Event**: Sends a custom behavioral event to HubSpot associated with that contact.

## Prerequisites

- **HubSpot Private App Access Token**: You must create a Private App in HubSpot with the following scopes:
  - `crm.objects.contacts.read`
  - `crm.objects.contacts.write`
  - `analytics.behavioral_events.send`
- **Email Address**: An email address is required as the primary identifier.

## Configuration

### Step 1: Contact Properties
Map your incoming event data to HubSpot Contact properties:
- **Email**: (Required) The unique identifier for the contact.
- **First/Last Name**: Basic identity fields.
- **Additional Properties**: A table to map any custom HubSpot internal property names to values from your event data.

### Step 2: Custom Behavioral Event
- **Internal Event Name**: The internal name of the event defined in HubSpot (e.g., `pe12345_my_event`).
- **Event Properties**: Add custom properties to the event to provide more context (e.g., product category, value, etc.).

## Features
- **Sequential Execution**: Ensures the contact is updated in the CRM before the event is fired, ensuring better data association.
- **Sandboxed JS**: Built using GTM's security-focused APIs.
- **Detailed Logging**: Built-in debug logging for the GTM Preview console.

## Support
For issues or feature requests, please open an issue on the GitHub repository.

---
*Disclaimer: This is a community-developed template and is not officially affiliated with HubSpot.*