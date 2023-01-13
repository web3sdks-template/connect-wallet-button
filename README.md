# Connect Wallet Button

This template shows you how you can use our `ConnectWallet` component from our React SDK to allow users to connect their wallet with your app with one of the following wallets:

- MetaMask
- Wallet Connect
- Coinbase Wallet

## Wrap Your Application in the Web3sdksProvider

```jsx
import { ChainId, Web3sdksProvider } from "@web3sdks/react";

// This is the chainId your dApp will work on.
const activeChainId = ChainId.Goerli;

function MyApp({ Component, pageProps }) {
  return (
    <Web3sdksProvider desiredChainId={activeChainId}>
      <Component {...pageProps} />
    </Web3sdksProvider>
  );
}

export default MyApp;
```

## Use the Connect Wallet Component!

```jsx
import { ConnectWallet } from "@web3sdks/react";

export default function Home() {
  return (
      <ConnectWallet accentColor="#f213a4" colorMode="dark" />
  );
}
```
