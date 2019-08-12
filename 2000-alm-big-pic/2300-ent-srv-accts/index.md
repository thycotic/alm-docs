[title]: # (Enterprise Service Accounts: Have Privileges, Will Travel)
[tags]: # (Account Lifecycle Manager,ALM,)
[priority]: # (2300)

## Enterprise Service Accounts: Have Privileges, Will Travel

Just as humans share their workstations with unseen agents using local workstation accounts, they share their networks with silent throngs of non-human agents authenticated to the network using enterprise service accounts.

* A service account supplies access to a computer process, not a person. The processes using service accounts make the digital lives of human users possible, performing thousands of tasks so that common activities, like sharing documents and printing reports, become effortless.

* When a computer process accesses protected resources, those resources prompt for an account and password before allowing the access, just as with people.

* The computer process likewise supplies credentials much as people do, sending a service account name and password to the resource.

Unfortunately, things quickly get messy when humans try to oversee accounts not used by actual people. Many human admins lose track of which non-human users do what tasks, and understandably so:

* Incomprehensibly named computer processes use often poorly named service accounts to access many resources to do many things, very many times, very quickly.

* Even when audit trails apply, service accounts often generate audit trails too enormous, dense, and cryptic for effective human review.

* Service accounts pile up because of uncertainty about which remain necessary. Suspending any of them might break or disable important services users need to work.

That is a bad outcome, but so is doing nothing. Many such accounts have substantial privileges—often the highest privileges possible—because many developers do not consistently apply least-privilege practices.

It gets worse. Too often, the uncompiled code behind the computer processes using service accounts remains exposed somewhere on the network—and that code sometimes contains the plain-text account names and passwords for each service account the developer thought the computer process might need to use.

* Hackers preferentially target service accounts for compromise, knowing they may lack effective monitoring and have elevated privileges.

* A malicious actor using a compromised service account can severely harm an organization.

* With its elevated privileges, a service account that helps make sending email effortless could make it just as effortless for an intruder to steal protected customer billing data.

This situation, entirely common at large organizations, may look like a Gordian Knot to network administrators. Loathe to risk disruptions that could impair business operations, they hesitate to deprivilege accounts of unknown purpose—yet they cannot ignore the security risks of leaving them active.

Solving this problem requires sustained effort in two areas:

* The organization must inventory and evaluate existing enterprise service accounts to determine whether they remain in use, and if so, whether they require adjustments to their privileges for conformance to least privilege principles.

* The organization must apply controls and standards to processes for creating, privileging, and retiring service accounts.

### ALM: Bringing PAM to Enterprise Service Accounts

Thycotic’s Account Lifecycle Manager service applies controls and standards to service account provisioning, allowing consistent application of least-privilege principles for these accounts.

* Using ALM structures an organization’s process for requesting and approving service accounts, as well as ensuring the prompt review, renewal, or expiration of service accounts.

* This halts the accumulation of forgotten, little-used, or unknown accounts.

* ALM also supports workflows to automate the structure it brings to account requests, approvals, and provisioning. This conserves staff time for tasks requiring human discernment and judgment, for example, reviewing audit trails to detect service account anomalies.

#### What About Existing Service Accounts?

When it comes to dealing with an extant collection of service accounts of unknown significance, there is no silver bullet. Organizations must examine these accounts individually and consult audit logs for clues to their purpose.

However, with ALM bringing order to the provisioning of new service accounts, the organization acquires a better understanding of its use of service accounts, in general. That helps in determining the provenance and continued relevance of existing accounts.

Furthermore, since most service accounts eventually expire, on consideration for renewal they become subject to the same provisioning rules the organization enforces via ALM for new service accounts. This eases the work of resolving the extant collection of service accounts by breaking it down as manageable, steadily paced piecework.

Moving forward, Secret Server also helps reduce the risks associated with service accounts by securing the service account credentials passed by software authenticating as these accounts.

