# Base PNET Holder-Distribution Snapshot

Status: public-chain snapshot; beneficial-owner labels remain incomplete

Capture block: `48,477,164`

Capture time: `2026-07-11 04:21:15 UTC`

Block hash: `0x83754ad647aa4dabd6a56978f934071e32bc2f8d754dfd44d8f691e302175cbe`

Asset: ProfitNet / `PNET` on Base, contract `0xe1F7F585f458cB6AFFCEE2286b8482523B19ee5a`

## Result

The Base ERC-20 ledger had ten addresses with a positive PNET balance at the capture block. That is an address count, not a count of people, independent buyers, or independent beneficial owners.

| Rank | Address | PNET balance | Supply share | Public interpretation at capture |
| ---: | --- | ---: | ---: | --- |
| 1 | [`0xd58cc829622c4c988af43028aaa37eda84104649`](https://basescan.org/address/0xd58cc829622c4c988af43028aaa37eda84104649) | `74,747,111.457500470910009950` | `74.747111457500%` | Initial-recipient smart-wallet address. The public dossier does not yet document its controller model or treasury policy. |
| 2 | [`0x7f97e32af1d2eb65d9d5f5b5ce15048768234a58`](https://basescan.org/address/0x7f97e32af1d2eb65d9d5f5b5ce15048768234a58) | `15,000,000` | `15.000000000000%` | Unlabelled externally owned address. Its project relationship, controller, purpose, and restrictions require maintainer confirmation. |
| 3 | [`0x777900c0ff11845c8e0d6c134b58c695023aab4e`](https://basescan.org/address/0x777900c0ff11845c8e0d6c134b58c695023aab4e) | `4,745,752.137568596788575110` | `4.745752137568%` | Uniswap CCA auction contract inventory; not an independent beneficial owner. Final bidder distribution is pending auction settlement. |
| 4 | [`0x34385dd739fe5464892bf0ba4cc42492804da000`](https://basescan.org/address/0x34385dd739fe5464892bf0ba4cc42492804da000) | `3,559,314.103176447591431331` | `3.559314103176%` | Auction LBP strategy inventory; not an independent beneficial owner. Final migration evidence is pending. |
| 5 | [`0x498581ff718922c3f8e6a244956af099b2652b2b`](https://basescan.org/address/0x498581ff718922c3f8e6a244956af099b2652b2b) | `1,947,813.470058203859406294` | `1.947813470058%` | Uniswap v4 PoolManager inventory. The singleton contract address is infrastructure, not an independent beneficial owner. |
| 6 | [`0xa568a959aa287f9004dbe9c5402b581083a0dc6f`](https://basescan.org/address/0xa568a959aa287f9004dbe9c5402b581083a0dc6f) | `6.755115987102991431` | `0.000006755115%` | Unlabelled address. |
| 7 | [`0x8fe83dab1d17185f091569b440b9e3c7ead1453d`](https://basescan.org/address/0x8fe83dab1d17185f091569b440b9e3c7ead1453d) | `1.043327601673784307` | `0.000001043327%` | Unlabelled address. |
| 8 | [`0x8b1fb4937bab5d02248a0825bf2564863237b00f`](https://basescan.org/address/0x8b1fb4937bab5d02248a0825bf2564863237b00f) | `1.022461049640308622` | `0.000001022461%` | Unlabelled address. |
| 9 | [`0xad01c20d5886137e056775af56915de824c8fce5`](https://basescan.org/address/0xad01c20d5886137e056775af56915de824c8fce5) | `0.010791642433492954` | `0.000000010791%` | Unlabelled address. |
| 10 | [`0x8f10b468b06c6fd214b65f87778827f7d113f996`](https://basescan.org/address/0x8f10b468b06c6fd214b65f87778827f7d113f996) | `0.000000000000000001` | less than `0.000000000001%` | Dust balance; not evidence of an independent holder. |
|  | **Total** | **`100,000,000`** | **`100%`** | Reconciles to `totalSupply()` at the capture block. |

The five small unlabelled balances total only `8.831696280850577315` PNET. Auction, LBP-strategy, and PoolManager inventory totals `10,252,879.710803248239412735` PNET, or `10.252879710803%` of supply. Those three contracts describe launch/liquidity mechanics; they must not be counted as three independent owners.

## Concentration Indicators

| Indicator | Address-level result | Interpretation |
| --- | ---: | --- |
| Largest address | `74.747111457500%` | One address alone holds more than half of total supply. |
| Two largest addresses | `89.747111457500%` | If the unlabelled 15,000,000-PNET address shares the same beneficial controller as the initial-recipient wallet, same-control concentration is at least this amount. That relationship is not yet established in this dossier. |
| Five largest addresses | `99.999991168303%` | Includes three launch/liquidity contracts, so this is not a five-person ownership measure. |
| Address-level Gini coefficient | approximately `0.814079` | Mechanical result over the ten positive address balances; contract inventory and controlled-wallet splitting can distort it. |
| Address-level Nakamoto coefficient for more than 50% | `1` | One address has more than 50%; this is not a governance analysis. |

To bring the largest address below 50% of fixed supply, at least `24,747,111.457500470910009950` PNET would need to leave that address for genuinely independent beneficial owners. Moving the same tokens among wallets controlled by the same person would not accomplish that. If the unlabelled 15,000,000-PNET address is under the same beneficial control, at least `39,747,111.457500470910009950` PNET would need to leave that combined control group to bring it below 50%.

The current auction inventory has already left the largest address. Even if all `4,745,752.137568596788575110` auction-contract PNET later reaches independent bidders, that event alone does not reduce the largest address's present `74.747111457500%` balance. It would, however, convert contract inventory into broader economic ownership if the bidders are genuinely independent.

## Method

1. Retrieved all 44 PNET `Transfer` records from deployment through block `48,477,164` with Blockscout's Base token-transfer API.
2. Reconstructed each address balance by adding incoming values and subtracting outgoing values, using the contract's `18` decimals.
3. Queried `balanceOf(address)` for every positive address with Base JSON-RPC at block tag `0x2e3b3ec` and reconciled the results to the transfer reconstruction.
4. Queried `totalSupply()` at the same block and confirmed `100,000,000` PNET.
5. Retrieved the block header at the same block tag to record its timestamp and hash.
6. Calculated concentration over positive ERC-20 address balances only. No attempt was made to infer people from addresses.

Sources:

- [BaseScan block 48,477,164](https://basescan.org/block/48477164)
- [Blockscout transfer query through the capture block](https://base.blockscout.com/api?module=account&action=tokentx&contractaddress=0xe1F7F585f458cB6AFFCEE2286b8482523B19ee5a&startblock=0&endblock=48477164&page=1&offset=10000&sort=asc)
- [Base public JSON-RPC endpoint](https://mainnet.base.org)
- [PNET verified source](https://basescan.org/address/0xe1F7F585f458cB6AFFCEE2286b8482523B19ee5a#code)
- [15,000,000-PNET transfer transaction](https://basescan.org/tx/0x8d2e6692ca874fc43208f8fb9172f0c84d1fc29cf1898dc0514a1876fb51df09)

The explorer's cached holder-ranking view was not used as the source of truth. Transfer reconstruction plus block-pinned contract calls makes the record reproducible even if an explorer's current holder page changes later.

## What This Snapshot Does Not Prove

- It does not prove which addresses are controlled by the same person or organization.
- It does not prove that any unlabelled address is independent, a buyer, a team wallet, or a treasury.
- It does not turn CCA, LBP-strategy, or PoolManager inventory into independent holders.
- It does not prove circulating supply; that requires a published treatment for treasury, auction, strategy, liquidity, vesting, and restricted balances.
- It does not prove that a Uniswap v4 position NFT is locked, burned, or inaccessible. ERC-20 `balanceOf` data cannot establish NFT ownership, timelock custody, unlock authority, or lock duration.
- It does not prove that the auction graduated, migrated, or created a final canonical pool. Those require settlement and migration transactions.

## Required Maintainer Follow-Up

1. Confirm whether `0x7f97e32af1d2eb65d9d5f5b5ce15048768234a58` is project-related. If it is, publish its role, beneficial-control category, intended use, and any vesting or transfer restriction. If it is not, publish only the supportable non-private label.
2. Publish a controlled-address registry covering treasury, team, auction, strategy, liquidity, vesting, grants, and operational addresses.
3. Publish Base-specific allocation and circulating-supply methodology rather than assuming the legacy Algorand allocation applies.
4. After the CCA resolves, publish the amounts sold and unsold, independently funded bidder count, bidder concentration, USDC raised, migration transaction, final pool ID, position owner, and exact lock evidence.
5. Refresh this snapshot after settlement and at regular dated intervals. Never manufacture improvement by splitting controlled balances or sending dust to new addresses.
