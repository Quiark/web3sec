# web3sec
Concise security summary for web3 users

## Attacks
### `eth_sig` signature forging
**Action steps**:
 - check that each wallet app you're using disables or disallows the `eth_sign` wallet API

**Risk**:
 - stolen ETH or any asset from your account after you've approved signature (of some long hex string) on a malicious website

**Non-risks**:
 - usually, full drain of wallet (all assets with one signature) will not happen (see Caveats)

### Signature phishing
**Action steps**:
 - revoke as many contracts using revoke.cash as possible
 - confirm that you're on the correct website (check URL) before any action in Metamask (or wallet)

**Risks**:
 - typically, selling a NFT on marketplace for a very low price
 - in principle, any other signature based action can be taken after you approve the sig. Voting, selling coins or NFTs, ...

**Non-risks**:
 - plain, unwrapped ETH cannot be transferred this way
 - usually, full drain of wallet (all assets with one signature) will not happen (see Caveats)


## Caveats
### Smart wallets, batch transfers, Permit2
