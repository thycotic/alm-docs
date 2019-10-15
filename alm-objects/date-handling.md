[title]: # (ALM Storage of Dates)
[tags]: # (Account Lifecycle Manager,ALM,Active Directory,)
[priority]: # (2500)

# ALM Storage of Dates

Dates and times at rest in the cloud (that is, in ALM storage) are UTC time.

When you work within the ALM UI, ALM handles the interpretation of UTC to local time for display in the ALM UI, and back to UTC for storage when you update a date and time via the ALM UI.

If you should happen to work directly with the API, note that a call that returns a date and time will return it in UTC.

Likewise, when working directly with the API, any date and time information you provide should be in UTC.




