[title]: # (Runaway Privileges at Endpoints)
[tags]: # (Account  Manager,ALM,)
[priority]: # (2200)

## Runaway Privileges at Endpoints

The typical user of an enterprise network signs on to a workstation using their enterprise user account credentials. Most have no inkling that they share the workstation with software entities signed on using credentials for service accounts local to the workstation.

* For example, antivirus software may be set up with a service account on the workstation so that it can run at all times, or Microsoft Office might have a service account it uses to interact with online extras.

When these local workstation service accounts have privileges greater than those needed to fulfill their purpose, risk accrues.

* Local accounts make easy targets; attacks on these accounts often go undetected.

* Once compromised, privileged local accounts provide a low-profile, high-risk vehicle for infiltration of the network.

* Yet these endpoint hazards often receive scant attention from network administrators.

### Privilege Manager: Bringing PAM to Endpoints

Thycotic’s Privilege Manager service helps organizations take back control of local account security excesses.

As an endpoint least privilege and application control solution for Windows and Macs, Privilege Manager allows administrators to automatically discover local administrator privileges and enforce least privilege principles through policy-driven actions.

So far, so good, but one more vulnerability, of a similar nature, remains beyond the reach of Secret Server and Privilege Manager.
