---
id: "walletaccount"
title: "WalletAccount"
sidebar_label: "WalletAccount"
---

## Hierarchy

* **WalletAccount**

## Index

### Constructors

* [constructor](walletaccount.md#constructor)

### Properties

* [_authData](walletaccount.md#_authdata)
* [_authDataKey](walletaccount.md#_authdatakey)
* [_keyStore](walletaccount.md#_keystore)
* [_networkId](walletaccount.md#_networkid)
* [_walletBaseUrl](walletaccount.md#_walletbaseurl)

### Methods

* [_completeSignInWithAccessKey](walletaccount.md#_completesigninwithaccesskey)
* [_moveKeyFromTempToPermanent](walletaccount.md#_movekeyfromtemptopermanent)
* [getAccountId](walletaccount.md#getaccountid)
* [isSignedIn](walletaccount.md#issignedin)
* [requestSignIn](walletaccount.md#requestsignin)
* [signOut](walletaccount.md#signout)

## Constructors

###  constructor

\+ **new WalletAccount**(`near`: [Near](near.md), `appKeyPrefix`: string | null): *[WalletAccount](walletaccount.md)*

*Defined in [wallet-account.ts:18](https://github.com/nearprotocol/nearlib/blob/88ad17d/src.ts/wallet-account.ts#L18)*

**Parameters:**

Name | Type |
------ | ------ |
`near` | [Near](near.md) |
`appKeyPrefix` | string &#124; null |

**Returns:** *[WalletAccount](walletaccount.md)*

## Properties

###  _authData

• **_authData**: *any*

*Defined in [wallet-account.ts:17](https://github.com/nearprotocol/nearlib/blob/88ad17d/src.ts/wallet-account.ts#L17)*

___

###  _authDataKey

• **_authDataKey**: *string*

*Defined in [wallet-account.ts:15](https://github.com/nearprotocol/nearlib/blob/88ad17d/src.ts/wallet-account.ts#L15)*

___

###  _keyStore

• **_keyStore**: *[KeyStore](keystore.md)*

*Defined in [wallet-account.ts:16](https://github.com/nearprotocol/nearlib/blob/88ad17d/src.ts/wallet-account.ts#L16)*

___

###  _networkId

• **_networkId**: *string*

*Defined in [wallet-account.ts:18](https://github.com/nearprotocol/nearlib/blob/88ad17d/src.ts/wallet-account.ts#L18)*

___

###  _walletBaseUrl

• **_walletBaseUrl**: *string*

*Defined in [wallet-account.ts:14](https://github.com/nearprotocol/nearlib/blob/88ad17d/src.ts/wallet-account.ts#L14)*

## Methods

###  _completeSignInWithAccessKey

▸ **_completeSignInWithAccessKey**(): *Promise‹void›*

*Defined in [wallet-account.ts:84](https://github.com/nearprotocol/nearlib/blob/88ad17d/src.ts/wallet-account.ts#L84)*

Complete sign in for a given account id and public key. To be invoked by the app when getting a callback from the wallet.

**Returns:** *Promise‹void›*

___

###  _moveKeyFromTempToPermanent

▸ **_moveKeyFromTempToPermanent**(`accountId`: string, `publicKey`: string): *Promise‹void›*

*Defined in [wallet-account.ts:97](https://github.com/nearprotocol/nearlib/blob/88ad17d/src.ts/wallet-account.ts#L97)*

**Parameters:**

Name | Type |
------ | ------ |
`accountId` | string |
`publicKey` | string |

**Returns:** *Promise‹void›*

___

###  getAccountId

▸ **getAccountId**(): *any*

*Defined in [wallet-account.ts:46](https://github.com/nearprotocol/nearlib/blob/88ad17d/src.ts/wallet-account.ts#L46)*

Returns authorized Account ID.

**`example`** 
walletAccount.getAccountId();

**Returns:** *any*

___

###  isSignedIn

▸ **isSignedIn**(): *boolean*

*Defined in [wallet-account.ts:37](https://github.com/nearprotocol/nearlib/blob/88ad17d/src.ts/wallet-account.ts#L37)*

Returns true, if this WalletAccount is authorized with the wallet.

**`example`** 
walletAccount.isSignedIn();

**Returns:** *boolean*

___

###  requestSignIn

▸ **requestSignIn**(`contractId`: string, `title`: string, `successUrl`: string, `failureUrl`: string): *Promise‹void›*

*Defined in [wallet-account.ts:63](https://github.com/nearprotocol/nearlib/blob/88ad17d/src.ts/wallet-account.ts#L63)*

Redirects current page to the wallet authentication page.

**`example`** 
  walletAccount.requestSignIn(
    myContractId,
    title,
    onSuccessHref,
    onFailureHref);

**Parameters:**

Name | Type | Description |
------ | ------ | ------ |
`contractId` | string | contract ID of the application |
`title` | string | name of the application |
`successUrl` | string | url to redirect on success |
`failureUrl` | string | url to redirect on failure |

**Returns:** *Promise‹void›*

___

###  signOut

▸ **signOut**(): *void*

*Defined in [wallet-account.ts:108](https://github.com/nearprotocol/nearlib/blob/88ad17d/src.ts/wallet-account.ts#L108)*

Sign out from the current account

**`example`** 
walletAccount.signOut();

**Returns:** *void*
