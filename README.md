![Banner](https://solrunner.bot/images/solrunner-text.png)

## SolRunner Solana Bot

[![TypeScript](https://badgen.net/badge/icon/typescript?icon=typescript&label)](https://typescriptlang.org)
![](https://img.shields.io/badge/soar-trading_bot-blue)
![UPTime](https://camo.githubusercontent.com/4a67ad96d71cca235a4393b2f3b79aabb0a3d42d555030632f1110e9eedde567/68747470733a2f2f696d672e736869656c64732e696f2f62616467652f757074696d652d3130302532352d627269676874677265656e)


[**SolRunner**](https://solrunner.bot/) that listens to new Raydium USDC or SOL pools and buys tokens for a fixed amount in USDC/SOL.

> *Depending on the speed of the RPC node, the purchase usually happens before the token is available on Raydium UI or Pump.fun for swapping.*

Official Website: [SolRunner.bot](https://solrunner.bot/)


# Features 🤖
- `Automatic snipe new pair pool`
- `Looks for profitable TXs and perform sandwich attack`
- `Copy trade from whale's wallets`
- `Stoploss & Takeprofit`
- `Filter by min & max liquidity`
- `Burn Check`
- `Renounce Check`
- `Fast Buy`


## Wallet 💷
First step:
1. Create a new Solana wallet
2. Transfer some SOL to this new wallet
3. Convert some SOL to USDC or WSOL (you need USDC or WSOL depending on the configuration in .env file)


## Configure settings file 📝 
You can easily edit settings from the beautiful UI we built!

![](https://solrunner.bot/images/solrunner-tool.png)

## Auto Sell 📈
By default, auto sell is enabled. If you want to disable it, you need to:
1. Change `AUTO SELL` to `false`
2. Update `MAX SELL RETRIES` to set the maximum number of retries for selling token
3. Update `AUTO SELL DELAY` to the number of milliseconds you want to wait before selling the token (this will sell the token after the specified delay. (+- RPC node speed)).

AUTO_SELL_DELAY to 0, token will be sold immediately after buy.
There is no guarantee that the token will be sold at a profit or even sold at all. The developer is not responsible for any losses incurred by using this feature.

## Common Issues 📚

> ### UNSUPPORTED RPC NODE
> If you see following error in your log file:  
> `Error: 410 Gone:  {"jsonrpc":"2.0","error":{"code": 410, "message":"The RPC call or parameters have been disabled."}`  
> It means your RPC node doesn't support methods needed to execute script.
> FIX: Change your RPC node. You can use Shyft, Helius or Quicknode.
> 
> ### NO TOKEN ACCOUNT
> If you see following error in your log file:  
> `Error: No SOL token account found in wallet: `  
> it means that your wallet not have USDC/WSOL token account.
> FIX: Go to [Jup.ag](https://jup.ag) and swap some SOL/USDC or SOL/WSOL.

## Help 📮
Discord: @SolRunner

## Website 🌐
[SolRunner.bot](https://solrunner.bot/)
