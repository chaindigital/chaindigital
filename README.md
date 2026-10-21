<p align="center">
  <img src="https://raw.githubusercontent.com/chaindigital/logo/main/CD-banner.png" alt="Chaindigital banner" />
</p>

<p align="center">
  <img width="100%" src="https://capsule-render.vercel.app/api?type=rect&color=0:0E4C75,50:56CCF2,100:2D9CDB&height=4&section=header"/>
</p>

<p align="center">
  <a href="https://chaindigital.tech"><b>chaindigital.tech</b></a> &nbsp;·&nbsp;
  <a href="https://github.com/chaindigital/endpoints">RPC · API · Snapshots</a> &nbsp;·&nbsp;
  <a href="https://docs.chaindigital.tech">Docs</a> &nbsp;·&nbsp;
  <a href="https://x.com/chaindigitalx">X</a> &nbsp;·&nbsp;
  <a href="https://medium.com/@chaindigital">Medium</a> &nbsp;·&nbsp;
  <a href="mailto:chaindigitalsystem@gmail.com">Email</a>
</p>

<br/>

Chain Digital is an independent validator operator. We run our own bare-metal infrastructure
and turn what our nodes see into public analytics: who signed, who missed, and whether a gap was local or network-wide.

<br/>

## Stake with us

Our three main networks. On each one, the foundation selected us through its own program.

<table>
<tr>
<td width="140" align="center"><b>Celestia</b><br/><sub>data availability</sub></td>
<td>
<b>Celestia Foundation Delegation Program, Cohort 7</b>, delegation active · <a href="https://forum.celestia.org/t/foundation-delegation-cohort-7-is-live/2232">announcement</a>
<br/><br/>
Mainnet validator, and the network where we build the most: analytics, public endpoints and node tooling.
See <a href="#built-for-celestia">Built for Celestia</a> below.
<br/><br/>
<a href="https://celestia.explorers.guru/validator/celestiavaloper1t0uga8qxyxacv50ljjjwjw9c2z9y07ekmrzp8u"><b>Delegate&nbsp;→</b></a> &nbsp;·&nbsp;
<a href="https://chaindigital.tech/chaintia/">CelestiaSignals</a>
</td>
</tr>
<tr>
<td width="140" align="center"><b>Monad</b><br/><sub>high-performance EVM</sub></td>
<td>
<b>Monad Foundation Validator Delegation Program (VDP)</b> · <a href="https://docs.monad.xyz/node-ops/validator-delegation-program">program</a>
<br/><br/>
Operators apply to the VDP and the Foundation selects them. It weighs testnet uptime, operating experience, monitoring and security processes, and geographic spread.
Validators it accepts receive Foundation delegation and must keep meeting its requirements: uptime above 98%, a capped commission and a testnet validator kept running.
Alongside the validator we run network analytics: <a href="https://chaindigital.tech/chainmonad.html">MonadSignals</a> covers uptime, timeouts and voting power concentration,
and our own <a href="https://github.com/chaindigital/monad-scanner">monad-scanner</a> reports execution-layer risk signals, each with its own severity and evidence.
<br/><br/>
<a href="https://monadvision.com/validator/0xe45532Ce20b547C2E39a41ceF9Ba7174c1153a2a"><b>Validator&nbsp;→</b></a> &nbsp;·&nbsp;
<a href="https://chaindigital.tech/chainmonad.html">MonadSignals</a> &nbsp;·&nbsp;
<a href="https://docs.chaindigital.tech/mainnets/monad">guide</a>
</td>
</tr>
<tr>
<td width="140" align="center"><b>Starknet</b><br/><sub>staking on L2</sub></td>
<td>
<b>StarkWare Delegation Program, Round 3</b> · <a href="https://x.com/StarkWareLtd/status/2091454223221137824">announcement</a>
<br/><br/>
Round 3 moved from breadth to depth. Each selected validator received 5M–20M STRK, with higher requirements for performance, reliability, testing and active participation.
<br/><br/>
<a href="https://voyager.online/staking?validator=0x023d2174be7e064dc31f3f358c850fc1ab3e05ad5b61ea7479e23843250845d0"><b>Delegate&nbsp;→</b></a>
</td>
</tr>
</table>

<sub>Commission and current terms are shown in each network's explorer.</sub>

We also validate on
[Dymension](https://dymension.explorers.guru/validator/dymvaloper1vpjnwwcqetkf6rtjcx4cvhd47l8ke06cynrun2),
[Lava](https://exp.stakevillage.net/lava-mainnet/staking/lava@valoper13gr2rrfeauy2q5qhzl03l5quzmcae466v0rgrf),
[Polkadot](https://polkadot.subscan.io/validator/16euDe2owvJq7LkwSujGxAFezCWopCKPENxwc2EKdzYTRBae),
[Kusama](https://kusama.subscan.io/validator/FHsDBsDmxzsANzvDrPBCzxyRAAYuTHCoe5d6vzi2qEdTBKk) and
[Gitopia](https://explorer.nodestake.org/gitopia/staking/gitopiavaloper1qqr9627fe9umfmx8h3ycd84g8e0u6q54sh8zxd).

<br/>

## Built for Celestia

#### [CelestiaSignals](https://chaindigital.tech/chaintia/): validator intelligence for mainnet

A live view of the active set, refreshed every 5 minutes from mainnet data. It shows voting power, missed blocks over 7 days and in total, proposer reliability, the top-10 share of voting power, and which Foundation delegation cohort each validator belongs to.

**Reports.** Generated automatically, and each one states its observation window:

| | |
|---|---|
| [**Weekly Validator Performance**](https://chaindigital.tech/chaintia/report28773) | Did validators process the blocks assigned to them? |
| [**Cohort Performance Analysis**](https://chaindigital.tech/chaintia/report84361) | Do delegation cohorts perform alike once workload is normalized? |
| [**Validator Network Proximity**](https://chaindigital.tech/chaintia/report29293) | Where is the reliable core of the set, and who falls outside it? |

Alongside them it keeps rolling snapshots: a missed-blocks overview, proposer reliability, and a consensus safety summary of jailed and tombstoned validators.

**CIP and upgrade readiness.** It tracks the official CIPs repository, with an operator watchlist of draft network upgrades and the live app version, so operators can see what to prepare for before an upgrade lands.

#### [endpoints](https://github.com/chaindigital/endpoints): RPC, API and snapshots

Public RPC and REST for mainnet and mocha-5, plus pruned `pebbledb` snapshots rebuilt every 6 hours, each with a checksum and a manifest.
Everything is collected on [chaindigital.tech/tools](https://chaindigital.tech/tools).

#### [celestia](https://github.com/chaindigital/celestia): node scripts

Install and upgrade scripts for validator, full and bridge nodes on mainnet and testnet, plus a monitoring setup.

<br/>

## How we sign

<p align="center">
  <img src="https://raw.githubusercontent.com/chaindigital/chaindigital/main/media/signing.svg?v=2" alt="Peers pass through sentries to a validator that holds no consensus key; TMKMS on an isolated host signs and returns only the signature" width="100%"/>
</p>

Dedicated bare metal on NVMe. Sentries and a private management network keep the validator away from the public internet.
Prometheus and Grafana alerts reach an on-call engineer. Configs live in Ansible and Terraform, and backups are restored as drills, not only written.
More in [server security for validators](https://docs.chaindigital.tech/validator-security/server-security-for-validators).

<br/>

## Repositories

- **[endpoints](https://github.com/chaindigital/endpoints)**: Celestia RPC, API and snapshots, with restore commands
- **[monad-scanner](https://github.com/chaindigital/monad-scanner)**: Monad block scanner for ordering, conflict and hot-state risk
- Node guides: [celestia](https://github.com/chaindigital/celestia) · [monad](https://github.com/chaindigital/monad) · [polkadot](https://github.com/chaindigital/polkadot) · [story](https://github.com/chaindigital/story) · [moonbeam](https://github.com/chaindigital/moonbeam)
- Upstream: [validator-info](https://github.com/chaindigital/validator-info) · [chain-registry](https://github.com/chaindigital/chain-registry) · [celestia-app](https://github.com/chaindigital/celestia-app) · [awesome-celestia](https://github.com/chaindigital/awesome-celestia)

<br/>

---

<p align="center">
  <sub>Distributed team across Thailand, Bali, Australia and Germany · on call 24/7</sub><br/>
  <sub><i>Reliability comes from engineering, not promises.</i></sub>
</p>

