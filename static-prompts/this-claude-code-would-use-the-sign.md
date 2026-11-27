This Claude Code would use the sign-in of a self-hosted runner's session, which this machine's managed settings do not allow:
they require a particular sign-in (forceLoginOrgUUID or forceLoginMethod).
To allow the runner's sign-in here, the machine's administrator can add "allowNestedModelAccessUnderForceLogin": true to this machine's managed settings. Set it on self-hosted runner hosts only, never in a profile that reaches people's own computers.
