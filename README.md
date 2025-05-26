# 🚀 Bot Setup Instructions

Welcome to the bot setup guide! Follow the steps below to install and configure the bot correctly. This guide is designed to be beginner-friendly, with clear explanations for each step.

> [Termux guides if you run on mobile](https://github.com/MeoMunDep/Guides-for-using-my-script-on-termux)

---

## Table of Contents

1. [Prerequisites](#prerequisites)
2. [Installation Steps](#installation-steps)
3. [Configuration Files](#configuration-files)
   - [`configs.json`](#1-configsjson)
   - [`privateKeys.txt`](#2-walletstxt)
   - [`proxies.txt`](#3-proxiestxt)
4. [Running the Bot](#running-the-bot)
5. [Contact and Support](#contact-and-support)

---

## Prerequisites

Before running the bot, make sure you have the following installed:

- **Node.js** (Version: `22.11.0`)
- **npm** (Version: `10.9.0`)

Download Node.js and npm here: [Download Link](https://t.me/KeoAirDropFreeNe/257/1462).

-> Double click on `run.bat` for windows or `run.sh` for linux/mac if you want to run automatically, remember to fill all the necessary data.

---

## Installation Steps

1. **Download and Extract the Bot Files:**

   - Extract the bot package into a folder on your computer.

2. **Install Dependencies:**
   Open your terminal or command prompt, navigate to the folder where the bot files are located, and run:

   ```bash
   npm install --force user-agents axios https-proxy-agent socks-proxy-agent meo-forkcy-colors ethers web3 
   ```

   If you encounter an Execution Policy error on Windows, run:

   ```bash
   Set-ExecutionPolicy -Scope Process -ExecutionPolicy Bypass
   ```

   Then, run the npm install command again.

3. **Prepare Configuration Files:**
   - Ensure all configuration files are set up correctly before running the bot (see [Configuration Files](#configuration-files) section).

---

## Configuration Files

### 1. `configs.json` - 📜 Adjust Bot Settings

This file controls the bot’s behavior. Below is an example configuration:

```json
{
  "rotateProxy": false,
  "skipInvalidProxy": false,
  "proxyRotationInterval": 2,
  "delayEachAccount": [1, 1],
  "timeToRestartAllAccounts": 300,
  "howManyAccountsRunInOneTime": 10,

  "bridgeAmount": [1, 5],
  "bridgeTime": [1, 5],
  "gasLimit": 100000,

   "faucet": {
    "maxCaptchaAttempts": 20,
    "2captchaApiKey": ""
  }
}
```

---

### Configuration Options

* `rotateProxy`: Enable or disable proxy rotation.

  * **false** means all accounts use a fixed proxy (or no proxy if unspecified).

* `skipInvalidProxy`: Skip invalid proxies if `true`.

  * **false** will stop the program if a proxy fails.

* `proxyRotationInterval`: Time interval (in **minutes**) for rotating proxies (only applies if `rotateProxy` is `true`).

  * Example: `2` means rotate every 2 minutes.

* `delayEachAccount`: Random delay range (in **seconds**) between starting each account.

  * Example: `[1, 1]` means a fixed 1-second delay.

* `timeToRestartAllAccounts`: Time (in **seconds**) to wait before restarting all accounts once finished.

  * Example: `300` means restart every 5 minutes.

* `howManyAccountsRunInOneTime`: Number of accounts to run in parallel at a time.

  * Example: `10` means run 10 accounts simultaneously.

---

### Faucet Settings

* `faucet.maxCaptchaAttempts`: Maximum number of attempts to solve CAPTCHA per account.

  * Example: `20`

* `faucet.2captchaApiKey`: Your 2Captcha API key for solving CAPTCHA challenges.

  * Leave it empty (`""`) to disable CAPTCHA solving.

---

### 2. `privateKeys.txt` - 💼 Wallet Addresses

- Wallets generator: [Link](https://github.com/MeoMunDep/Automatic-Ultimate-Create-Wallets-for-Airdrop)
- Add your wallet addresses in the following format:

```txt
EVM privatekey
EVM privatekey
EVM privatekey
```

_Note: Wallet updates are currently not supported._

### 3. `proxies.txt` - 🌐 Proxy List (Optional)

If you are using proxies, add them here. Leave the file blank if you are not using proxies. Supported formats:

- [Get it from here](https://www.webshare.io/?referral_code=4l5kb3glsce7)

```txt
http://host:port
https://host:port
socks4://host:port
socks5://host:port
http://user:pass@host:port
https://user:pass@host:port
socks4://user:pass@host:port
socks5://user:pass@host:port
```

_Note: each row for each account_

---

## Running the Bot

1. Navigate to the folder containing the bot files:

   ```bash
   cd /path/to/hybrid
   ```

2. Run the bot using the following command:
   ```bash
   node tx_meomundep.js
   ```

---

## Contact and Support

- **Help me with your referral** [Referral Link](https://t.me/HybridMiniAppBot/HybridMiniApp?startapp=6713068747&text=Join%20the%20Hybrid%20Mini%20App,%20and%20let%E2%80%99s%20earn%20together!%20Use%20my%20invite%20link%20to%20join%20the%20fun%20%0A%0ATake%20your%20welcome%20bonus:%20%0A%F0%9F%92%B8%2010,000%20Coins%20%0A%F0%9F%94%A5%2015,000%20Coins%20if%20you%20have%20Telegram%20Premium)
- **Buy me a telegram account** [Here](https://t.me/KeoAirDropFreeNe/312/27801) or [Here](https://github.com/MeoMunDep/MeoMunDep)

If you encounter any issues or have questions, feel free to reach out:

- **Contact:** [Contact Me](https://t.me/MeoMunDep)
- **Group:** [Join the Group](https://t.me/KeoAirDropFreeNe)
- **Channel:** [Visit the Channel](https://t.me/KeoAirDropFreeNee)

Your support is greatly appreciated! 🐱

---

Enjoy using the bot! 🚀
