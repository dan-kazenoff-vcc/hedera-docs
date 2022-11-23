# SystemDelete

## SystemDeleteTransactionBody

Delete a file or smart contract - can only be done with a Hedera administrative multisignature. When it is deleted, it immediately disappears from the system as seen by the user, but is still stored internally until the expiration time, at which time it is truly and permanently deleted. Until that time, it can be undeleted by the Hedera administrative multisignature. When a smart contract is deleted, the cryptocurrency account within it continues to exist, and is not affected by the expiration time here.

| Field            | Type                                                                                                                                                | Description                                                                              |
| ---------------- | --------------------------------------------------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------- |
| `id`             | **one of:**                                                                                                                                         |                                                                                          |
|                  | [FileID](https://github.com/theekrystallee/hedera-style-guide/blob/sdk-v1/deprecated/hedera-api/miscellaneous/broken-reference/README.md)           | The file ID of the file to delete, in the format used in transactions                    |
|                  | [ContractID](https://github.com/theekrystallee/hedera-style-guide/blob/sdk-v1/deprecated/hedera-api/miscellaneous/broken-reference/README.md)       | The contract ID instance to delete, in the format used in transactions                   |
| `expirationTime` | [TimestampSeconds](https://github.com/theekrystallee/hedera-style-guide/blob/sdk-v1/deprecated/hedera-api/miscellaneous/broken-reference/README.md) | The timestamp in seconds at which the "deleted" file should truly be permanently deleted |