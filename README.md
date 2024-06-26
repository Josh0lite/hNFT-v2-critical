## UserAccountsController2

**Version2:**
- Fixed some errors.
- Added security cryptography.
- And some more stuff.

**Owner:**[Yuri-DaBang](https://github.com/Yuri-DaBang)


## Some Stuff
- **[HttpPost("auth")]**: Handles user authentication, comparing credentials and returning an authentication token and user object if successful.

- **[HttpPost("add-money/{username}")]**: Adds 1 unit of money to the specified user's account balance.

- **[HttpPost("deduct-money/{username}")]**: Deducts 1 unit of money from the specified user's account if sufficient funds are available.

- **[HttpPost("send-money")]**: Transfers money between users based on a `MoneyTransferRequest` object in the request body.

- **[HttpPost("save-user-data")]**: Saves updated user account data back to `UsrAccounts.json`.

- **Helper Method**: `IsUserAuthenticated` checks if a user is authenticated based on an authentication token (`authToken`).

- **UserAccount Class**: Represents a user account with properties for username, password, account balance, and account lock status.

- **MoneyTransferRequest Class**: Represents a money transfer request with properties for sender, recipient, and amount.

- **Note**: Some endpoints like `GetUserBalance`, `LockUserAccount`, and `UnlockUserAccount` are commented out and may be non-functional.
