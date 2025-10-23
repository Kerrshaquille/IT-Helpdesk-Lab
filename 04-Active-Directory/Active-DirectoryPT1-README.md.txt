# Active Directory Installation & User Management

## Lab Setup Documentation

-----

## 1. Install Active Directory Domain Services

**Action:** Add Roles and Features

- Opened Server Manager
- Selected “Add roles and features”
- Proceeded through installation wizard

**Screenshot:** `01-add-roles-and-features.png`

-----

## 2. Active Directory Domain Services Selection

**Role Selected:**

- ✅ Active Directory Domain Services (checkbox checked)

Required features automatically added.

**Screenshot:** `02-ad-domain-services-checkbox.png`

-----

## 3. Promote Server to Domain Controller

**Post-Installation Action:**

- Active Directory Domain Services installed successfully
- Clicked notification flag: “Promote this server to a domain controller”

**Screenshot:** `03-promote-to-domain-controller.png`

-----

## 4. Deployment Configuration

**Forest Configuration:**

- **Deployment Type:** Add a new forest
- **Root Domain Name:** KHTech.com

**Screenshot:** `04-deployment-config-khtech.png`

-----

## 5. Domain Controller Installation Complete

**Domain Installed:**

- Domain: KHTech.com
- Administrator Account: KHTECH\Administrator
- Server restarted automatically

**Screenshot:** `05-domain-installed-khtech-admin.png`

-----

## 6. Active Directory Administrative Center

Opened Active Directory Administrative Center for domain management.

**Screenshot:** `06-ad-administrative-center.png`

-----

## 7. Active Directory Administrative Center - Domain View

Navigated to local domain (KHTech.com) in Administrative Center.

**Screenshot:** `07-ad-admin-center-domain-local.png`

-----

## 8. Enable Active Directory Recycle Bin

**Action:** Enabled Recycle Bin feature

**Purpose:**

- Allows recovery of deleted Active Directory objects
- Preserves all object attributes during recovery
- Eliminates need for authoritative restore from backup

**Screenshot:** `08-enable-recycle-bin.png`

-----

## 9. Active Directory Users and Computers

Opened Active Directory Users and Computers console for user management.

**Screenshot:** `09-ad-users-and-computers.png`

-----

## 10. Create New User Account

**Action:** Right-click → New → User

Initiated user account creation process.

**Screenshot:** `10-create-new-user.png`

-----

## 11. User Account Created - Kathy

**User Details:**

- **Username:** Kathy
- **Domain:** KHTech.com
- Account successfully created in Active Directory

**Screenshot:** `11-user-created-kathy.png`

-----

## 12. Reset User Password

**Action:** Right-click user → Reset Password

Demonstrated password reset procedure for user account.

**Screenshot:** `12-reset-password.png`

-----

## 13. Disable User Account

**Action:** Right-click user → Disable Account

Account disabled - user cannot log in.

- Account marked with red “X” icon

**Screenshot:** `13-disable-account.png`

-----

## 14. Enable User Account

**Action:** Right-click user → Enable Account

Previously disabled account re-enabled - user can now log in.

- Red “X” icon removed

**Screenshot:** `14-enable-account.png`

-----

## 15. Account Options

Opened user account properties to view and configure account options:

- Account expiration
- Logon hours
- Password policies
- Account lockout status

**Screenshot:** `15-account-options.png`

-----

## Summary

✅ Active Directory Domain Services installed
✅ Server promoted to Domain Controller
✅ Domain created: KHTech.com
✅ Active Directory Recycle Bin enabled
✅ User account created (Kathy)
✅ Password reset procedure demonstrated
✅ Account disable/enable procedures demonstrated
✅ Account options reviewed

-----

## Skills Demonstrated

### Active Directory Administration

- AD DS installation and configuration
- Domain Controller promotion
- Forest creation and management
- Active Directory Recycle Bin configuration

### User Account Management

- User account creation
- Password management and reset procedures
- Account enable/disable operations
- User account properties configuration

### Help Desk Tier 1/2 Skills

- New user onboarding (account creation)
- Password reset support
- Account lockout troubleshooting
- Account status management (enable/disable)

-----

## Next Steps

- [ ] Create additional user accounts
- [ ] Configure user properties (contact info, department)
- [ ] Create Organizational Units (OUs)
- [ ] Set up security groups
- [ ] Configure Group Policy Objects
- [ ] Join Windows 10 client to domain

-----

## Screenshots

All screenshots referenced in this documentation are located in:
`04-Active-Directory/screenshots/`