# web3sec
Concise security summary for web3 users

## Attacks
### `eth_sig` signature forging
**Action steps**:
 - check that each wallet app you're using disables or disallows the `eth_sign` wallet API

**Risk**:
 - stolen ETH or any asset from your account after you've confirmed the signature (of some long hex string) on a malicious website using your wallet

**Non-risks**:
 - usually, full drain of wallet (all assets gone with one signature) will not happen (see Caveats)

### Signature phishing
**Action steps**:
 - revoke as many contracts using revoke.cash as possible
 - confirm that you're on the correct website (check URL) before any action in Metamask (or wallet)

**Risks**:
 - typically, selling a NFT on marketplace for a very low price
 - in principle, any other signature based action can be taken after you confirm the sig in MM. Voting, selling coins or NFTs, ...

**Non-risks**:
 - plain, unwrapped ETH cannot be transferred this way
 - usually, full drain of wallet (all assets gone with one signature) will not happen (see Caveats)

### YOLO signing on HW wallet
You got your Ledger/Trezor/... as everyone has been telling you but then you don't really check what you're signing on the device and those buttons are so tiny and annoying, just click click done.

**Risks**:
 - You just signed something else than what you saw on Metamask wallet and the coins go to an attacker! Turns out your computer got compromised and showed you fake info!

**Action steps**:
 - Verify transaction details on the tiny screen of the HW wallet device each time. I know this is annoying and complicated but it will significantly improve your security.

## Caveats
### Smart wallets, batch transfers, Permit2
Uniswap's Permit2 contract, SAFE multisig wallet and upcoming ERC-4337 account abstraction and others may allow transferring multiple assets at once, making full drain possible in one transaction.
However, they are all opt-in, you need to be using that kind of wallet or have a token approval for it to be possible.

## Advanced security precautions

These tips go a little beyond what normal computer users are recommended to do but frankly if you're in crypto, you're gonna need it.

- To combat phishing, add all your important websites to bookmarks. Banks, email, work sites, DeFi apps. Verify the URL is correct. After that, *ONLY* ever go to that website via your trusted bookmark. Got an email asking you to do something in your bank acc? Sure, open browser and click your bookmark. Ignore link in email.
- Login screen for bank / gmail / ... suddenly shows up? Well, I don't log in when they ask me. I log in by clicking my bookmark on a new tab first.
- Multiple browsers. Use Firefox for work stuff, separate Chrome profile for crypto, another browser for risky / lewd sites. Another clean browser or profile with no extension for going to the bank.
- (pro Windows users) Check your computer for malware yourself. (optional) get [Process Explorer](https://learn.microsoft.com/en-us/sysinternals/downloads/process-explorer) and learn to recognise every process there. Where is it from? Later you can find if there's some new process, that may be malware.
- (pro users) Consider using a more intrusive firewall like [GlassWire](https://www.glasswire.com/) or Little Snitch. It will ask you to approve every single network connection. Kinda annoying but can potentially stop something.
