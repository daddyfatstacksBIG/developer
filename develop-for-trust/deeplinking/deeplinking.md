# Deeplinking

All deeplink routes can be used with either `https://link.trustwallet.com` or `trust://`.

The `https://link.trustwallet.com` domain will route the user to a download landing page where the user can download the app for iOS, Android, or web extension. If the user already has the app installed, they will get a pop-up deeplinking them to the actual route page in the app.

The `trust://` URI will directly deeplink route the user to the corresponding in-app page and should be used in campaigns where it is known that all users clicking on the link already have the Trust Wallet app installed.

## DApp Browser

Open dapp browser with a specific url and network

- `coin` slip44 index
- `url` website url

`https://link.trustwallet.com/open_url?coin_id=60&url=https://compound.finance`

## Assets

### Open coin

- `asset` asset in [UAI format](/assets/universal_asset_id.md)

`https://link.trustwallet.com/open_coin?asset=c60`

### Add asset

Asset will be added to local storage and will show up on the wallet screen.

- `asset` asset in [UAI format](/assets/universal_asset_id.md)

`https://link.trustwallet.com/add_asset?asset=c60_t0x514910771af9ca656af840dff83e8264ecf986ca`

## Payment

### Redeem Code:

- `code` unique code
- `provider` provider url

`https://link.trustwallet.com/redeem?code=abc123`

### Send Payment:

- `asset` asset in [UAI format](/assets/universal_asset_id.md)
- `address` Recipient address
- `amount` Optional. Payment amount
- `memo` Optional. Memo
- `data` Optional. Data

`https://link.trustwallet.com/send?asset=c60_t0x6B175474E89094C44Da98b954EedeAC495271d0F&address=0x650b5e446edabad7eba7fa7bb2f6119b2630bfbb&amount=1&memo=test`

### Referral:

`https://link.trustwallet.com/referral`

## Staking

### Stake details:

- `coin` slip44 index

`https://link.trustwallet.com/stake?coin=118`

### Stake / Delegate:

- `coin` slip44 index
- `id` validator / delegator to be selected. Optional

`https://link.trustwallet.com/stake_delegate?coin=118&id=cosmosvaloper156gqf9837u7d4c4678yt3rl4ls9c5vuursrrzf`

### Unstake / Undelegate:

- `coin` slip44 index

`https://link.trustwallet.com/stake_undelegate?coin=118`

### Claim Rewards:

- `coin` slip44 index

`https://link.trustwallet.com/stake_claim_rewards?coin=118`

## Exchange

### Open Swap:

- `from` asset in [UAI format](/assets/universal_asset_id.md)
- `to` asset in [UAI format](/assets/universal_asset_id.md)

`https://link.trustwallet.com/swap?from=c60_t0x6B175474E89094C44Da98b954EedeAC495271d0F&to=c60`

### Open Buy Crypto

- `asset` asset in [UAI format](/assets/universal_asset_id.md)
- `provider` Specifies the fiat ramp provider (e.g., moonpay, mercuryo, ramp). Optional.
- `payment_method` Specifies the payment method (e.g., credit_card, bank_transfer, apple_pay, google_pay, digital_wallet). Optional.
- `sub_payment_method` Specifies the sub payment method (e.g., paypal, skrill, blik). Optional.
- `fiat_currency` Specifies the currency for the amount (e.g., USD, GBP). Optional.
- `fiat_quantity` Specifies the default quantity of the asset to buy (e.g., 3, 0.25). Optional.

`https://link.trustwallet.com/buy?asset=c60&provider=moonpay&payment_method=digital_wallet&sub_payment_method=paypal&fiat_currency=USD&fiat_quantity=300`

### Open Sell Crypto

- `asset` asset in [UAI format](/assets/universal_asset_id.md)

`https://link.trustwallet.com/sell?asset=c60_t0x6B175474E89094C44Da98b954EedeAC495271d0F`

### Open Market Info

- `asset` asset in [UAI format](/assets/universal_asset_id.md)

`https://link.trustwallet.com/market?asset=c60_t0x6B175474E89094C44Da98b954EedeAC495271d0F`

### Open Notifications

`https://link.trustwallet.com/notifications`

### Open Price alerts

`https://link.trustwallet.com/alerts`

## WalletConnect

### Connect to a WalletConnect session

`https://link.trustwallet.com/wc?uri=wc%3Aca1fccc0-f4d1-46c2-90b7-c07fce1c0cae%401%3Fbridge%3Dhttps%253A%252F%252Fbridge.walletconnect.org%26key%3Da413d90751839c7628873557c718fd73fcedc5e8e8c07cfecaefc0d3a178b1d8`

## NFTs

Open NFTs tab.

`https://link.trustwallet.com/nfts`

## Quest

Open the quest page.

`https://link.trustwallet.com/quest`

## Launchpool

Open the Launchpool page.

`https://link.trustwallet.com/launchpool`

## Hot Tokens

Open the Hot Tokens tab on the Swap page.

`https://link.trustwallet.com/hot_tokens`

### Open Hot category and all networks

- `category_id` category identifier

`https://link.trustwallet.com/hot_tokens?category_id=hot`

### Open Hot category and specific network

- `category_id` category identifier
- `network` network identifier (slip44 index)

`https://link.trustwallet.com/hot_tokens?category_id=hot&network=c0`

## Settings

### Open the notification settings page

`https://link.trustwallet.com/notification_settings`
