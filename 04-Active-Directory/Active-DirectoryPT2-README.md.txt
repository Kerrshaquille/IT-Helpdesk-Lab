# Active Directory Part 2 - Advanced Account Management

## User Account Testing & Troubleshooting Scenarios

-----

## Overview

This documentation covers advanced Active Directory user account management scenarios commonly encountered in help desk support. All scenarios use test user account “Kathy” to demonstrate various account states and troubleshooting procedures.

-----

## 1. User Account Disabled

**Scenario:** Administrator disabled Kathy’s account

**Account Status:**

- Account marked with red “X” icon in Active Directory
- User cannot authenticate
- Login attempts will fail with “account disabled” message

**Use Case:**

- Employee termination
- Security incident response
- Temporary access suspension

**Screenshot:** `01-user-kathy-account-disabled.png`

-----

## 2. Account Enabled - Logon Denied

**Scenario:** Account re-enabled but login still denied

**Possible Causes:**

- Logon hours restriction active
- Workstation restrictions in place
- Group policy preventing login
- Account not yet synchronized across domain

**Troubleshooting Action:**

- Verified account enabled in AD
- Checked for additional restrictions
- Identified logon time/location restrictions

**Screenshot:** `02-user-kathy-account-enabled-logon-denied.png`

-----

## 3. Account Time Restriction

**Configuration:** Logon hours restriction applied to Kathy’s account

**Purpose:**

- Limit when user can authenticate
- Enforce business hours access
- Enhance security by restricting off-hours access
- Common for temporary/contractor accounts

**Settings:**

- Configured permitted logon hours
- Outside permitted hours: authentication denied
- Inside permitted hours: login allowed

**Screenshot:** `03-user-kathy-account-time-restriction.png`

-----

## 4. Account Expired

**Scenario:** Account expiration date reached

**Account Status:**

- Account expiration date configured
- Date passed - account automatically disabled
- User cannot log in
- Common for temporary employees/contractors

**Configuration:**

- Account Properties → Account tab → Account expires
- Set specific expiration date
- After date: login automatically denied

**Screenshot:** `04-user-kathy-account-expired.png`

-----

## 5. User Login Successful

**Scenario:** All restrictions removed/resolved - successful authentication

**Verification:**

- Account enabled ✅
- No time restrictions preventing login ✅
- Account not expired ✅
- Account not locked ✅
- User authenticated successfully ✅

**Result:**

- Domain user logged in successfully
- Desktop loaded properly
- Access to network resources available

**Screenshot:** `05-user-kathy-login-successful.png`

-----

## 6. Account Locked Out

**Scenario:** Account locked due to multiple failed login attempts

**Cause:**

- Exceeded maximum failed login attempts (defined in Group Policy)
- Common reasons: forgotten password, caps lock on, old password cached

**Account Status:**

- Account Properties shows “Unlock account” checkbox
- Checkbox is checked (indicating locked state)
- User cannot log in until unlocked
- May auto-unlock after lockout duration expires

**Screenshot:** `06-user-kathy-account-locked-out.png`

-----

## 7. Account Unlocked

**Resolution:** Administrator manually unlocked the account

**Procedure:**

1. Opened user account properties in AD
1. Navigated to Account tab
1. Checked “Unlock account” checkbox
1. Applied changes
1. User can now attempt login again

**Best Practice:**

- Verify user identity before unlocking
- May want to reset password if multiple lockouts occur
- Document lockout incidents for security tracking

**Screenshot:** `07-user-kathy-account-unlocked.png`

-----

## Summary

### Account States Demonstrated

✅ Account disabled (administrative action)
✅ Account enabled with logon restrictions
✅ Logon hours/time restrictions configured
✅ Account expiration configured and triggered
✅ Successful login after restrictions removed
✅ Account lockout due to failed login attempts
✅ Account unlock procedure

-----

## Help Desk Skills Practiced

### Tier 1 Support

- Account unlock procedures
- Password reset (related to lockouts)
- Account status verification
- Basic troubleshooting of login issues

### Tier 2 Support

- Account expiration management
- Logon hours configuration
- Account enable/disable procedures
- Complex authentication troubleshooting

### Security Practices

- Understanding account lockout policies
- Recognizing security incidents (multiple lockouts)
- Proper account lifecycle management
- Access control implementation

-----

## Common Help Desk Tickets Simulated

### Ticket 1: “I can’t log in - account disabled”

**Issue:** Account disabled
**Resolution:** Verified reason for disable, re-enabled account per manager approval
**Demonstrated in:** Screenshot 01-02

### Ticket 2: “Login works sometimes but not others”

**Issue:** Logon hours restriction
**Resolution:** Identified time restrictions, explained policy to user or modified per business need
**Demonstrated in:** Screenshot 03

### Ticket 3: “Former contractor can’t access system”

**Issue:** Account expired
**Resolution:** Identified expiration date, extended date or created new account per policy
**Demonstrated in:** Screenshot 04

### Ticket 4: “Account locked - can’t log in”

**Issue:** Account lockout after failed login attempts
**Resolution:** Unlocked account, assisted with password reset if needed
**Demonstrated in:** Screenshot 06-07

-----

## Troubleshooting Methodology Demonstrated

### Step 1: Identify Symptom

- User reports inability to log in
- Specific error message collected

### Step 2: Check Account Status

- Open Active Directory Users and Computers
- Locate user account
- Check for visual indicators (red X, icons)

### Step 3: Review Account Properties

- Account tab: Check enabled status, expiration, lockout
- Logon hours: Check time restrictions
- Account options: Review password policies

### Step 4: Apply Resolution

- Unlock if locked
- Enable if disabled
- Extend expiration if expired
- Modify logon hours if restricted

### Step 5: Verify Resolution

- Test user login
- Confirm successful authentication
- Document resolution

-----

## Key Concepts

### Account Lockout Policy

- Defined in Group Policy
- Specifies threshold (e.g., 5 failed attempts)
- Lockout duration (e.g., 30 minutes)
- Can be manually unlocked by administrator

### Account Expiration

- Proactive security measure
- Automatically disables account on set date
- Common for temporary workers
- Requires manual extension or re-enable

### Logon Hours

- Restricts when user can authenticate
- Does NOT forcibly log off active sessions
- Prevents NEW logins outside permitted hours
- Useful for shift workers or security policies

### Account Disabled vs Locked

- **Disabled:** Manual administrative action, requires manual re-enable
- **Locked:** Automatic response to failed logins, may auto-unlock or requires manual unlock

-----

## Active Directory Account Properties Referenced

### Account Tab

- User logon name
- Account options (disabled, locked)
- Account expires settings
- Logon hours configuration
- Unlock account checkbox

### Account Options Explored

- Account is disabled
- Account is locked out
- Password never expires
- User cannot change password
- Account expires on [date]

-----

## Next Steps

- [ ] Configure Group Policy for account lockout threshold
- [ ] Set up email notifications for account lockouts
- [ ] Create account expiration process for contractors
- [ ] Document standard operating procedures for each scenario
- [ ] Practice additional account management tasks

-----

## Screenshots

All screenshots referenced in this documentation are located in:
`04-Active-Directory/screenshots/` (or dedicated subfolder if created)

-----

## Portfolio Value

**This demonstrates:**

- Comprehensive understanding of Active Directory account lifecycle
- Practical troubleshooting of authentication issues
- Security-conscious account management practices
- Ability to diagnose and resolve multiple account state issues
- Real-world help desk problem-solving skills

**Employer Takeaway:** Candidate has hands-on experience with common AD account issues and can independently troubleshoot authentication problems - critical for help desk tiers 1 and 2.