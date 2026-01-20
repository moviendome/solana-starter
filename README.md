# Create a Fungible Token

## Setup

### Create turbin3-wallet.json
#### Create new Keypair

```bash
solana-keygen new --outfile turbin3-wallet.json
```

```
Wrote new keypair to turbin3-wallet.json
=====================================================================
pubkey: FqgrMQgCvEMYaUhsa3WBQsqwQbLfVKbGEWB2etpHC12
=====================================================================
Save this seed phrase and your BIP39 passphrase to recover your new keypair:
****
=====================================================================
```

#### View Public Key
```
solana-keygen pubkey turbin3-wallet.json
```

```
FqgrMQgCvEMYaUhsa3WBQsqwQbLfVKbGEWB2etpHC12
```


### Fund the wallet

```bash
npx ts-node prereqs/airdrop.ts
```


---

## Create a Fungible Token

### Create mint

```
npx ts-node cluster1/spl_init.ts
```

```
Mint created: 7MRPbbekVZ7E8uNj9WVcoURT8tJqYtM19LqruHPqkHS7
```

### Mint tokens
```
npx ts-node cluster1/spl_mint.ts
```

```
Your ata is: CdgV1ZPavtSzAqnMyER7umAzecW93FJdzkbQyWFhmpsx
Your mint txid: 5UQJfcf11LBQnTkyCYmr3PcAdparoccaZZ7HQwTvjK8GXUfsRbtLb39tjzCuoXEa7cXSxjP9KjstmNxhioGGTq9S
```

---

## Checklist

- [x] Create wallet
- [x] Fund wallet
- [x] Create mint
- [x] Update mint address in `spl_mint.ts`
- [x] Mint tokens
- [x] Verify tokens on Solana Explorer (devnet)

## Solana Explorer

- [Token Account](https://explorer.solana.com/address/CdgV1ZPavtSzAqnMyER7umAzecW93FJdzkbQyWFhmpsx?cluster=devnet)
- [Transaction](https://explorer.solana.com/tx/5UQJfcf11LBQnTkyCYmr3PcAdparoccaZZ7HQwTvjK8GXUfsRbtLb39tjzCuoXEa7cXSxjP9KjstmNxhioGGTq9S?cluster=devnet)
