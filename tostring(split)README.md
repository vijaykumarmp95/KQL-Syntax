//Query snippet showing how to extract the account name from an email address

AccountName = tostring(split(RecipientEmailAddress, "@")[0])

====================================================================================

EmailEvents
| where Timestamp > ago(7d)
| project RecipientEmailAddress, AccountName = tostring(split(RecipientEmailAddress, "@")[0]);
