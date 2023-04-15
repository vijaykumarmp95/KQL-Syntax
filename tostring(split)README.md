//Query snippet showing how to extract the account name from an email address ( to get "Raju" from "raju@abc.com")

AccountName = tostring(split(RecipientEmailAddress, "@")[0])

====================================================================================

EmailEvents

| where Timestamp > ago(7d)

| project RecipientEmailAddress, AccountName = tostring(split(RecipientEmailAddress, "@")[0])

========================================================================================
OUTPUT

RecepientEmailAddress     Accountname

raju@abc.com              Raju
kapoor@abc.com            Kapoor
