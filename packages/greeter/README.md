# Greeter Tutorial

`greeter` is a simple demo of Arbitrum's L1-to-L2 message passing system (aka "retryable tickets").

It deploys 2 contracts - one to L1, and another to L2, and has the L1 contract send a message to the L2 contract to be executed automatically.

The script and contracts demonstrate how to interact with Arbitrum's core bridge contracts to create these retryable messages, how to calculate and forward appropriate fees from L1 to L2, and how to use Arbitrum's L1-to-L2 message [address aliasing](https://developer.offchainlabs.com/docs/l1_l2_messages#address-aliasing).

See [./exec.js](./scripts/exec.js) for inline explanation.

[Click here](https://developer.offchainlabs.com/docs/l1_l2_messages) for more info on retryable tickets.

### Run Demo:

- Send a message from `L1` to `L2`
```
yarn run greeterFromL1
```

- Send a message from `L2` to `L1`. 

> With non-native token (ETH), we don't need to execute outbox manually,
> The system is auto redeem for us. Wait more than a day and check L1 Greeter

```
yarn run greeterFromL2
```

## Config Environment Variables

Set the values shown in `.env-sample` as environmental variables. To copy it into a `.env` file:

```bash
cp .env-sample .env
```

(you'll still need to edit some variables, i.e., `DEVNET_PRIVKEY`)

<p align="center"><img src="../../assets/offchain_labs_logo.png" width="600"></p>