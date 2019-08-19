[title]: # (Modern IT and Least Privileged Access)
[tags]: # (Account Lifecycle Manager,ALM,)
[priority]: # (2100)

## Modern IT and Least Privileged Access

The principle of Least Privileged Access holds that users of protected systems (the computers and the network) should have the minimum access privileges needed to perform their work:

* When users have access to systems for which they have no business need, the risk increases that a careless or malicious user will abuse that access to cause harm.

* Therefore, in an ideal environment, user accounts will have privileges adequate for the tasks the account user must perform—and no more.

* Modern IT embraces this idea, but most organizations face multiple barriers to conforming the enterprise to least privilege.

Typically, complex directory services software (such as Active Directory) nominally control access to the enterprise. In practice, diverse other applications and systems require users to additionally authenticate. Password proliferation results.

Frustrated by how many passwords they must remember, users develop habits that reduce security, such as:

* relying on weak passwords

* writing passwords down where others can discover them

* sharing their passwords with other people

* transmitting their passwords across dubious networks

### Secret Server: Restoring the Power of Passwords by Making Them Vanish

Enter Secret Server, Thycotic’s flagship product. Secret Server counters the adverse effects of password proliferation on user security behavior, offering to generate strong passwords whenever a user sets up credentials for a protected resource. Secret Server stores the passwords, or “secrets,” in a vault securely located in the cloud. Later, when a resource prompts for a password, Secret Server provides it.

This setup replaces many user authentication tasks with just one login to Secret Server per work session. Commonly, this means users will sign in with Secret Server right after they log in to the enterprise, such as by logging in to a workstation. After the Secret Server sign-in, they access resources almost as though passwords were not required.

* Users no longer need to remember so many passwords. Passwords seem to go away, with most never seen by human eyes.

* Sharing passwords becomes a useful practice, not a forbidden breach. For example, a supervisor schedules time off and directs Secret Server to share the supervisor’s passwords with an assistant. Sharing the password makes it available for use without revealing it to the person using it. On returning to work, the supervisor simply unshares the password.

   * Audit logs record which supervisor authentications were for a work session of the supervisor, and which were for a work session of the assistant.

   * In practical terms, this amounts to **secure password sharing**—three words, once oxymoronic, now describing a breakthrough addition to the utility of passwords.

Put simply, Secret Server protects users from themselves—unburdening them of passwords, so that passwords seem to vanish—while restoring the power of passwords to protect systems, and even extending their power by enabling secure password sharing.

Yet, even with all user passwords being strong, always “remembered,” and securely stored in the cloud, and even with all users adhering to proper security practices, password related threats remain.




