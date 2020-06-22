# ActiveRoles and Safeguard for Just-in-time Access
Active Roles Just-in-Time Provisioning for Safeguard allows privileges to be assigned at the time of a credential check-out.  Accounts in AD that will require privileges to perform a function (i.e. Domain Admin) will be added to the appropriate group(s) when the the account is approved for check out in Safeguard.  This applies to both password requests and session requests. 

This is accomplished by adding the "to be privileged" user account to the appropriate group as required, then removed when no longer required.  This further secures the AD environment from privilege escalation attacks.

This project provides a simple listener service, `ARSGJitAccess`, which subscribes to Safeguard password request events. When a PasswordRequest is approved by Safeguard, the `ARSGJitAccess` calls Active Roles to set a (configurable) `ARSGJITAccessAttribute` on the privileged account. Active Roles is configured to make dynamic group membership changes based on the value of the `ARSGJITAccessAttribute` 

## Watch the video
Please watch the following video to see a demonstration of the just-in-time access solution:

[Just the Demo Video](https://oneidentity.github.io/ActiveRoles-Safeguard-JIT-Access/demo.html "Demo Video")

## Install and Config
Please watch the following video to learn how you can set up ActiveRoles-Safeguard-JIT-Access:

[Full Install and Config Video](https://oneidentity.github.io/ActiveRoles-Safeguard-JIT-Access/install.html "Install Video")

## Support
One Identity open source projects are supported through One Identity GitHub issues and the One Identity Community. This includes all scripts, plugins, SDKs, modules, code snippets or other solutions. For assistance with any One Identity GitHub project, please raise a new Issue on the One Identity GitHub project page. You may also visit the One Identity Community to ask questions. Requests for assistance made through official One Identity Support will be referred back to GitHub and the One Identity Community forums where those requests can benefit all users.
