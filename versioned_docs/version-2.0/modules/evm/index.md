---
id: "index"
title: "Evm Module"
sidebar_label: "EVM"
sidebar_position: 0
custom_edit_url: null
toc_max_heading_level: 4
---

```js
Moralis.Evm.xxx()
```

### General
#### web3Library

Returns web3 library in use

```js
Moralis.Evm.web3Library()
```

#### connectors

Connect to EVM via connector


Register the connector like:

  ```javascript
  import WalletConnectConnector from '@moralisweb3/evm-wallet-connect-connector';
  Moralis.Evm.connectors.register(WalletConnectConnector);
  ```

**Output in console**

```js
Moralis[evmConnector: metamask]: Connecting 
{providedOptions: {…}, options: {…}}
options: {silent: false, timeout: 30000, _options: {…}}
providedOptions: {silent: false}
```

If you wish to remove them (not recommended but there might be an exotic use-case):

```javascript
Moralis.Evm.connectors.remove('wallet-connect'); // Use the name of the connector
```

#### supportedConnectors

Get name of all supportedConnectors

```js
Moralis.Evm.supportedConnectors()
```

#### connector

Get info on connector

```js
Moralis.Evm.connector()
```

**Output in console**

```js
account: EvmAddress {_value: '0x93905fd3f9b8732015f2b3Ca6c16Cbcb60ECf895'}
chain: EvmChain {_value: '0x5', _chainlistData: {…}}
core: MoralisCore {name: 'core', modules: MoralisModules, registerModules: ƒ, registerModule: ƒ, start: ƒ, …}
handleAccountsChanged: ƒ ()
handleChainChanged: ƒ ()
handleConnect: ƒ ()
handleDisconnect: ƒ ()
isSubscribedToEvents: true
logger: Logger {moduleName: 'evmConnector: metamask', core: MoralisCore}
name: "metamask"
network: "evm"
_events: Events {accountChanged: EE, chainChanged: EE}
_eventsCount: 2
_provider: Proxy {_events: {…}, _eventsCount: 4, _maxListeners: 100, _log: u, _state: {…}, …}
```


#### provider

Get info on connection provider

```js
Moralis.Evm.provider()
```

**Output in console**

```js
JsonRpcSigner {_isSigner: true, provider: Web3Provider, _address: '0x93905fd3f9b8732015f2b3Ca6c16Cbcb60ECf895', _index: null}
provider: Web3Provider {_isProvider: true, _events: Array(0), _emitted: {…}, disableCcipRead: false, formatter: Formatter, …}
_address: "0x93905fd3f9b8732015f2b3Ca6c16Cbcb60ECf895"
_index: null
_isSigner: true
[[Prototype]]: Signer
```

#### hasProvider

Check whether web3 provider exist

```js
Moralis.Evm.hasProvider()
```

#### chain

Get chain id

```js
Moralis.Evm.chain()
```

**Output in console**

```js
EvmChain {_value: '0x5', _chainlistData: {…}}
_chainlistData: {name: 'Görli', title: 'Ethereum Testnet Görli', chain: 'ETH', network: 'testnet', rpc: Array(3), …}
_value: "0x5"
apiHex: (...)
currency: (...)
decimal: (...)
explorer: (...)
hex: (...)
name: (...)
rpcUrls: (...)
[[Prototype]]: Object
```

#### account

Get account address of connected wallet

```js
Moralis.Evm.account()
```

**Output in console**

```js
EvmAddress {_value: '0x93905fd3f9b8732015f2b3Ca6c16Cbcb60ECf895'}
_value: "0x93905fd3f9b8732015f2b3Ca6c16Cbcb60ECf895"
checksum: (...)
lowercase: (...)
[[Prototype]]: Object
```

#### isConnected

Check whether web3 provider is connected or not

```js
Moralis.Evm.isConnected()
```


#### isConnecting

Get the connecting status of web3 provider

```js
Moralis.Evm.isConnecting()
```

### Event Listeners
#### onConnecting

Listen to events while web3 provider is connecting

```js
Moralis.Evm.onConnecting()
```

#### onConnected

Listen to events post web3 provider is connection

```js
Moralis.Evm.onConnected()
```


#### onDisconnected

Listen to events post web3 provider is disconnection

```js
Moralis.Evm.onDisconnected()
```


#### onConnectingError

Listen to events on web3 provider is connection error

```js
Moralis.Evm.onConnectingError()
```

#### onAccountChanged

Listen to events on changing account 

```js
Moralis.Evm.onAccountChanged()
```

#### onChainChanged

Listen to events when an evm chain is changed

```js
Moralis.Evm.onAccountChanged()
```


#### onProviderUpdated

Listen to events when web3 provider is updated

```js
Moralis.Evm.onProviderUpdated()
```



### Connection Methods
#### connect
#### disconnect

### Chain Methods
#### signMessage
#### sendTransaction
#### transferNative
#### transferErc20
#### transferErc721
#### transferErc1155
#### executeFunction

