# Pantheon Support Request

A WordPress plugin that creates a support request form specifically designed for Pantheon-hosted websites. The plugin collects environment information (Dev/Test/Live) along with WordPress and server details to help your support team quickly diagnose issues.

** Development server: ** https://dev-pantheon-support-request-plugin.pantheonsite.io/wp-admin/
** Username: ** `pantheon-support-request-plugin`

## Features

- **Simple Form**: Easy-to-use form for users to submit support requests
- **Pantheon-specific**: Includes Pantheon environment selection (Dev/Test/Live)
- **Advanced Email Delivery**: Configurable SMTP settings for reliable message delivery
- **System Information**: Automatically collects WordPress and server information to aid troubleshooting
- **Admin Interface**: Clean, tabbed settings page for easy configuration

## Installation

1. Download the plugin files
2. Upload the plugin folder to the `/wp-content/plugins/` directory of your WordPress installation
3. Activate the plugin through the 'Plugins' menu in WordPress
4. Configure the plugin settings through the 'Settings > Pantheon Support' menu

## Configuration

### General Settings

1. Navigate to **Settings > Pantheon Support** in your WordPress admin
2. Configure the following settings:
   - **Recipient Email**: The email address where support requests will be sent
   - **Email Subject**: The subject line for support request emails
   - **Include WordPress Info**: Toggle to include WordPress version, theme, and plugin information
   - **Include Server Info**: Toggle to include server details and environment information

### SMTP Configuration

For more reliable email delivery, configure the SMTP settings:

1. Go to the **SMTP** tab in the plugin settings
2. Enable the SMTP option
3. Configure your SMTP server details:
   - Host (e.g., smtp.gmail.com)
   - Port (typically 587 for TLS or 465 for SSL)
   - Encryption (TLS, SSL, or None)
   - Username and Password
4. Use the "Send Test Email" button to verify your settings

## Using the Form

Add the support form to any page or post using the shortcode:

```
[pantheon_support_form]
```

The form includes the following fields:
- Name
- Email
- Pantheon Environment (dropdown with Dev/Test/Live options)
- Message

## Email Content

When a user submits a request, the plugin sends an email with:

1. **User-submitted details**:
   - Name
   - Email
   - Selected Pantheon environment
   - Support message

2. **WordPress information** (if enabled):
   - WordPress version
   - Active theme and version
   - List of active plugins
   - Site URLs

3. **Server information** (if enabled):
   - PHP version
   - Server software
   - MySQL version
   - Key server variables

## Frequently Asked Questions

### How do I configure Gmail SMTP?

For Gmail SMTP, use these settings:
- SMTP Host: smtp.gmail.com
- SMTP Port: 587
- Encryption: TLS
- Username: your-email@gmail.com
- Password: your app password (requires 2FA and app password setup in your Google account)

### Does this work on Pantheon's environment?

Yes, this plugin is specifically designed for Pantheon-hosted WordPress sites and collects environment-specific information.

### Can I customize the form fields?

The current version includes fixed fields. Custom fields may be added in future releases.

## Troubleshooting

### Test emails are not being sent

1. Verify your SMTP credentials are correct
2. Ensure the port is not blocked by your hosting environment
3. For Gmail, ensure you're using an App Password if 2FA is enabled
4. Check that the recipient email address is correct

### Form submissions not showing up

1. Check your spam/junk folder
2. Verify the recipient email address in the plugin settings
3. Try configuring SMTP for more reliable delivery

## Changelog

### 1.0
* Initial release
* Basic form functionality
* SMTP configuration
* WordPress and server information collection

## Credits

Developed for Pantheon WordPress sites to streamline the support request process.

## License

This plugin is licensed under the GPL v2 or later.

```
This program is free software; you can redistribute it and/or
modify it under the terms of the GNU General Public License
as published by the Free Software Foundation; either version 2
of the License, or (at your option) any later version.

This program is distributed in the hope that it will be useful,
but WITHOUT ANY WARRANTY; without even the implied warranty of
MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the
GNU General Public License for more details.
```
