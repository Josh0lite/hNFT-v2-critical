## UserAccountsController2

**Version2:**
- Fixed some errors.
- Added security cryptography.
- And some more stuff.

**Owner:**[Yuri-DaBang](https://github.com/Yuri-DaBang)


## Ua Controller
- **[HttpPost("auth")]**: Handles user authentication, comparing credentials and returning an authentication token and user object if successful.

- **[HttpPost("add-money/{username}")]**: Adds 1 unit of money to the specified user's account balance.

- **[HttpPost("deduct-money/{username}")]**: Deducts 1 unit of money from the specified user's account if sufficient funds are available.

- **[HttpPost("send-money")]**: Transfers money between users based on a `MoneyTransferRequest` object in the request body.

- **[HttpPost("save-user-data")]**: Saves updated user account data back to `UsrAccounts.json`.

- **Helper Method**: `IsUserAuthenticated` checks if a user is authenticated based on an authentication token (`authToken`).

- **UserAccount Class**: Represents a user account with properties for username, password, account balance, and account lock status.

- **MoneyTransferRequest Class**: Represents a money transfer request with properties for sender, recipient, and amount.

- **Note**: Some endpoints like `GetUserBalance`, `LockUserAccount`, and `UnlockUserAccount` are commented out and may be non-functional.

## hNFT Controller

- **[HttpPost("account/auth")]**: Handles user authentication, comparing credentials and returning an authentication token and user object if successful.

- **[HttpPost("account/create")]**: Creates a new user account based on the provided `CreateUserRequest` object.

- **[HttpPost("account/email/update/{userId}")]**: Updates the email address of the specified user.

- **[HttpPost("account/asset/add/{userId}")]**: Adds a new asset to the specified user's account.

- **[HttpDelete("account/asset/remove/{userId}/{assetId}")]**: Removes an asset from the specified user's account.

- **[HttpPost("account/password/reset/{userId}")]**: Resets the password of the specified user.

- **[HttpGet("account/details/{userId}")]**: Retrieves the details of the specified user.

- **[HttpGet("account/assets/{userId}")]**: Lists all assets of the specified user.

- **[HttpGet("account/social/{userId}")]**: Retrieves the social information of the specified user.

- **[HttpPost("account/social/set/{userId}")]**: Sets the social information of the specified user.

- **[HttpGet("account/market/{userId}")]**: Gets market information related to the specified user's assets.

- **[HttpPost("account/bank/transfer")]**: Transfers an asset from one user to another based on the provided `TransferRequest` object.

- **[HttpGet("account/dashboard/{userId}")]**: Redirects the user to their dashboard.

- **[HttpPost("account/delete/{userId}")]**: Deletes (locks) the specified user account.

**Helper Method**

- **IsUserAuthenticated**: Checks if a user is authenticated based on an authentication token (`authToken`).

**Classes**

- **UserAccount Class**: Represents a user account with properties for username, password, account balance, and account lock status.

- **MoneyTransferRequest Class**: Represents a money transfer request with properties for sender, recipient, and amount.

## Note

Some endpoints like `GetUserBalance`, `LockUserAccount`, and `UnlockUserAccount` are commented out and may be non-functional.
