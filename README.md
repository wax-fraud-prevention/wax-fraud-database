# WAX Fraud Database

The WAX Fraud Database is a community-driven project to track and report fraudulent accounts and collections on the WAX Blockchain.  

The database is maintained by the WAX community and is open to contributions from anyone.

<p align="center">
  <img src="https://avatars.githubusercontent.com/u/161926701?s=300" />
</p>


## How does this work?

This repository provides json files containing the data of fraudulent accounts and collections.

You can use these files in your application to check if an account or collection is fraudulent and the reason they are on the list.


## How can I use this database?

There are two main ways to use this database.

> ### Option 1
> Load the json files directly from this repository in your application.  
This is recommended as it will always give you the most up-to-date information.
>
> https://raw.githubusercontent.com/wax-fraud-prevention/wax-fraud-database/main/wallets.json  
> https://raw.githubusercontent.com/wax-fraud-prevention/wax-fraud-database/main/collections.json

> ### Option 2
> Download the json files and use them in your application to check if an account or collection is fraudulent.  
This requires you to keep the json files updated manually in your application.


## How do I add an account or collection?

To add an account or collection to the database, you can create a pull request with the following information added to the appropriate json file.

Reasons should be short and to the point, do not include any personal information or links. Please keep reasons in English.

You can also add a level of either `danger` or `warning` to indicate the severity of the fraudulent activity.

- `danger` - The account or collection is known to be fraudulent and should be avoided at all costs.
- `warning` - The account or collection is suspicious and should be avoided until further information is available.

Any entries without a level should be considered as `danger`.

You may add additional information in the pull request description if you feel it is necessary. 

```json
{
    "name": "<accountname>",
    "level": "<danger, warning>",
    "reason": "<reason for being on the list>"
}
```

Example:
```json
{
    "name": "waxdropbybit",
    "level": "danger",
    "reason": "Scammer operating pig slaughter scam"
}
```


## When will my pull request be accepted?

All pull requests will be reviewed by the maintainers of this repository.

If the reason is clear and the account or collection is known to be fraudulent, the pull request will be accepted and the account or collection will be added to the database.

In cases where the reason is not clear, the maintainers may ask for more information in the pull request.

