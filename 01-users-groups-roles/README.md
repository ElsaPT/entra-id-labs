# Lab 01 – Users, Groups and Roles in Microsoft Entra ID

## Objective
Practise creating users and security groups in Microsoft Entra ID, add a test user to a group, and assign it a built-in least-privilege role (Reports Reader).

> **Note:** the role was assigned directly to the user, not to the group, because the free tenant (Entra ID Free) does not allow assigning roles to groups.

## What I did
1. Created a test user (`TestOne`) in the free tenant, with an auto-generated password.
2. Created a security group (`TestOne`) with Assigned membership and added the user as a member.
3. Assigned the built-in Reports Reader role to the user.
4. Signed in as `TestOne` in a private browser window and confirmed that the "New user" button was disabled, which shows the role gives read-only access.

## What went wrong
The test user's password was rejected on the first attempt because it included an accented character (ç). Entra ID only accepts ASCII characters, so I replaced it and the password was accepted. Apart from this, there were no obstacles.

## What I learned
- Password rules require at least 8 characters, 3 of the 4 character types (uppercase, lowercase, numbers, symbols), and the password cannot contain the user name.
- Assigned membership means members are added manually, while dynamic membership uses rules and needs a P1 licence.
- Least privilege: Reports Reader can read sign-in and audit reports but cannot create or change users.
- Assigning roles to groups is not available in the free tenant.
