# etherspot-stablecoins-tokenlist
Etherspot SDK StableCoins token list

Web: [https://etherspot.io](https://etherspot.io)

Docs: [https://docs.etherspot.dev/](https://docs.etherspot.dev/)

Use Etherspot SDK to fetch stable coins: 

```
import { Sdk, NetworkNames, randomPrivateKey } from 'etherspot';
const privateKey = randomPrivateKey();
let sdk: Sdk
sdk = new Sdk({
  privateKey,
  }, {
    networkName: 'mainnet' as NetworkNames,
    });
async function main() {
  const output = await sdk.getTokenListTokens({
    name: 'EtherspotStableCoins',
  });

  console.log('token list tokens', output);
}

main().catch(console.error);
