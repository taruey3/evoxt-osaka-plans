# Osaka VPS: Is $2.99/Month Enough, Which Evoxt Plan Fits, and When Is $49.99/Month Routing Worth It? (Full Plan Table + Buying Notes)

Evoxt's Osaka line runs from **$2.99/month** for 512 MB up to $95.99/month for 16 cores and 32 GB. The plan most readers should buy is **VM-1 at $5.99/month**: 1 core, 2 GB RAM, 20 GB SSD, 500 GB of monthly transfer, weekly backups included. If your users are on China Telecom and the route into China decides whether the project works, the number to compare against is **$49.99/month**, the entry price of an Osaka CN2 GIA plan from BandwagonHost. That is about eight times VM-1, and nothing on Evoxt's pricing page claims that route.

Below: the full eleven-plan table with the Osaka transfer allowances, which differ from Evoxt's standard regions; what "Premium Network" does and does not mean; five Osaka operators side by side with verified prices and contract terms; and the cases where you should not buy Evoxt at all.

> **Quick pick.** DNS, a WireGuard endpoint, or a box to measure Osaka latency before committing → VM-0.5, $2.99/mo. One small site, a bot, or a Docker stack → VM-1, $5.99/mo. Several sites plus a database → VM-2, $11.99/mo for 4 GB. 👉 [See the Osaka plan list and current prices](https://bit.ly/EvoXt)

## Evoxt Osaka plans and prices

All eleven plans are sold for Osaka (and Hong Kong) under the Premium Network tier. Prices are USD per month, and every tier includes weekly backups.

| Plan | vCPU / RAM | SSD | Transfer (Osaka) | Price | Order |
| --- | --- | --- | --- | --- | --- |
| VM-0.5 | 1 / 512 MB | 5 GB | 250 GB | $2.99/mo | [ Order VM-0.5](https://bit.ly/EvoXt) |
| VM-0.75 | 1 / 1 GB | 10 GB | 250 GB | $4.99/mo | [ Order VM-0.75](https://bit.ly/EvoXt) |
| VM-1 | 1 / 2 GB | 20 GB | 500 GB | $5.99/mo | [ Order VM-1](https://bit.ly/EvoXt) |
| VM-1.5 | 2 / 2 GB | 20 GB | 500 GB | $6.95/mo | [ Order VM-1.5](https://bit.ly/EvoXt) |
| VM-2 | 2 / 4 GB | 30 GB | 1,000 GB | $11.99/mo | [ Order VM-2](https://bit.ly/EvoXt) |
| VM-3 | 4 / 4 GB | 30 GB | 1,000 GB | $14.99/mo | [ Order VM-3](https://bit.ly/EvoXt) |
| VM-4 | 4 / 8 GB | 60 GB | 2,000 GB | $23.99/mo | [ Order VM-4](https://bit.ly/EvoXt) |
| VM-6 | 8 / 8 GB | 60 GB | 2,000 GB | $29.99/mo | [ Order VM-6](https://bit.ly/EvoXt) |
| VM-8 | 8 / 16 GB | 80 GB | 3,000 GB | $47.99/mo | [ Order VM-8](https://bit.ly/EvoXt) |
| VM-12 | 16 / 16 GB | 80 GB | 3,000 GB | $60.95/mo | [ Order VM-12](https://bit.ly/EvoXt) |
| VM-16 | 16 / 32 GB | 100 GB | 5,000 GB | $95.99/mo | [ Order VM-16](https://bit.ly/EvoXt) |

Two things in that table are worth more than the CPU column.

**The Osaka transfer caps are half the standard-region caps.** VM-1 gets 500 GB here, against 1,000 GB for the same plan name in Evoxt's standard regions; VM-0.5 gets 250 GB against 500 GB. The pattern holds all the way up: VM-4 is 2,000 GB in Osaka and twice that elsewhere. This is the real reason to size up from VM-1 rather than just adding RAM.

**VM-1.5 is the cheapest upgrade in the lineup.** For $0.96 more per month over VM-1, you go from one core to two with the same 2 GB of RAM and the same 500 GB of transfer. If you compile anything, run a JVM, or host more than one container that can spike, that dollar is the best value on the page. If you only serve static files or run a single lightweight app, you will not notice the second core.

Payment is by credit card, debit card, PayPal, Bitcoin, or USDt on Tron. Evoxt bills monthly up to a three-year term and lets you top up account credit that the system applies to future invoices, which is useful if you want to prepay without committing a single long invoice.

👉 [Choose a plan and confirm Osaka stock at checkout](https://bit.ly/EvoXt)

## What the table does not tell you about the contract

Evoxt's pricing page lists one price per configuration. There is no struck-through first-term price and no separate annual rate, so the $5.99 shown for VM-1 is what the plan costs. That is a good sign for renewal, but the invoice preview before you pay is the authoritative number, and it is the only place to confirm what a second term costs.

Three things are not published on the pricing page at all: a refund policy, an uptime SLA, and IPv6 allocation. If any of those decide the purchase for you, ask support before you pay for a three-year term. A monthly cycle costs the same per month as any longer one, so there is no financial penalty for starting monthly and only prepaying once you know the machine behaves.

Capacity is also the one variable you cannot check from a table. Osaka sits in the Premium tier alongside Hong Kong, and Evoxt's resellers list every Osaka plan with a "check availability" note rather than a stock count. Confirm the region is selectable in the cart before you enter payment details.

## "Premium Network" is a tier name, not a China route

Evoxt labels Osaka and Hong Kong as Premium Network. The pricing page does not list upstream carriers, peering exchanges, or a China-optimized route for Osaka, and nothing in the plan list mentions CN2 GIA, CTGNet, or a specific Chinese carrier. Buy the $5.99 plan because it is cheap and in Japan. Do not buy it expecting a China Telecom premium path, because that claim is not made.

Osaka is not one product, and the clearest proof is BandwagonHost running two tiers inside the same building, Equinix OS1. JPOS_1 belongs to its E-Commerce tier and rides Softbank plus Equinix IX, Google, Cloudflare and NTT; it is the older node and has a short, clean path to China Unicom. JPOS_6 belongs to the Ultra tier and adds China Telecom CN2 GIA / CTGNet on top of the same exchange mix, and that is the tier most people mean when they search for an Osaka VPS for Chinese visitors. Both are KVM with the in-house KiwiVM panel, both self-managed.

The price gap inside that one building is the whole argument. Ultra entry is $49.99/month or $499.99/year for 2 cores, 2 GB RAM, 40 GB SSD and 500 GB of transfer, and the yearly cycle saves roughly 17%. Plan 3, at 6 cores, 8 GB, 160 GB SSD and 2 TB, is $165.99/month or $1,665.99/year. Third-party tests on the CN2 GIA tier recorded roughly 33–36 ms from Shanghai Telecom, about 60 ms from Beijing Telecom, 52 ms from Beijing Unicom, and around 96–105 ms from China Mobile, with no loss across the samples. Those are third-party measurements on one sample, not a provider guarantee, and Osaka carries no 99.99% SLA in BandwagonHost's lineup; only its USCA_5 location does.

So the decision rule is blunt. If most of your traffic is mainland China on Telecom and latency is the product, pay the $49.99 and stop reading. If your visitors are in Japan, Korea, Southeast Asia, or you just need a Japanese IP for a service that has nothing to do with China, Evoxt's $2.99–$6.95 band covers it at a fraction of the cost.

👉 [Check what $5.99 buys in Osaka before you compare premium routes](https://bit.ly/EvoXt)

## Five Osaka operators, verified prices and catches

| Provider | Osaka site | Network notes | Entry price | Contract and catch |
| --- | --- | --- | --- | --- |
| Evoxt | Osaka / Hong Kong Premium tier | Carriers not published | $2.99/mo | Monthly to 3 years, weekly backup, no SLA published |
| BandwagonHost (Ultra, JPOS_6) | Equinix OS1 | CN2 GIA / CTGNet plus Equinix IX | $49.99/mo or $499.99/yr | Yearly saves ~17%, self-managed, no 99.99% SLA |
| Hostiger (OSA1) | Greater Osaka | JPIX Osaka, BBIX Osaka, tier-1 transit | Not listed on the region page | Hourly billing, reserved on activation, non-refundable, 99.99% SLA |
| Echelon (OSA1) | Dojima | NTT, IIJ, JPNAP Osaka | €1.90/mo on a 12-month term (€22.80 prepaid) | Email-only signup, 42 crypto assets, no KYC, 3:1 oversubscription on fair-share plans |
| v.ps | Equinix OS1 | AS4785, IIJ upstream, BBIX Osaka peering | Cloud KVM €6.95/mo, Edge KVM €8.95/mo | 99.9% SLA, 14-day refund window |

The Echelon number is the one that makes Evoxt look expensive. €1.90/month for 2 GB RAM, 25 GB NVMe and 2 TB of traffic beats VM-1 on paper by a wide margin. Read the contract column: that rate requires paying €22.80 up front for twelve months, which is fine if you already know you want a year of Osaka, and awkward if you are still testing whether Osaka is the right city. Echelon also runs 3:1 oversubscription on its fair-share plans, keeps port 25 closed until you open a ticket, sells extra IPv4 at €1.20/month, and takes signups by email with crypto payment only. Evoxt publishes no oversubscription ratio either, bills monthly, takes cards and PayPal, and includes weekly backups.

Put the three low-end options next to each other and the trade is clear. Echelon is €22.80 prepaid for a year of 2 GB. Evoxt is $5.99 month to month for 2 GB with half the storage and a quarter of the traffic. BandwagonHost is $49.99 a month for the same 2 GB with a China Telecom backbone attached. The specs are nearly identical across all three; the routing and the commitment are not.

Hostiger is the one to watch if you need an SLA and unmetered bandwidth rather than a low sticker price. Its OSA1 site sits in Greater Osaka with JPIX Osaka and BBIX Osaka peering, 1 Gbps unmetered symmetric, NVMe Gen4, APPI compliance and a 99.99% SLA. A 30-day benchmark on its 2 vCPU / 4 GB Pro plan recorded 9 ms 95th-percentile ping inside Kansai, 312k IOPS on 4K random writes and 947 Mbps through iperf3. No prices appear on the Osaka region page, and compute is reserved on activation, so the plan is non-refundable. v.ps sits in the same Equinix OS1 building with IIJ upstream and a 14-day refund window, at €6.95/month for Cloud KVM.

## Which Evoxt plan fits your workload

**VM-0.5, $2.99.** A DNS resolver, a WireGuard or Tailscale exit node, an uptime monitor, or a throwaway box to ping Osaka from the inside before you commit to a bigger plan. 512 MB runs Alpine and a single static binary happily and nothing else. A WordPress install with MySQL will swap from the first page load.

**VM-1, $5.99.** The default. A static site behind Nginx, a small WordPress with a page cache, a Telegram or Discord bot, a Docker Compose stack with two or three services. 2 GB is the point where a normal LEMP site stops touching swap under light traffic, and 500 GB of transfer covers roughly 16 GB a day.

**VM-1.5, $6.95.** Same RAM, same disk, one more core for under a dollar. Take it if you build from source, run Java, or host something that benefits from a second thread. Skip it if you are serving cached HTML.

**VM-2, $11.99.** 4 GB and 1,000 GB of transfer. Several sites on one box, a small Postgres or MySQL that actually gets queried, a game server for a handful of friends. This is where a single VPS can replace two small ones without constant tuning.

**VM-4 and above, $23.99+.** 8 GB is the first tier that behaves like a production host with Redis, a queue worker and a database on the same machine. Below 8 GB you are planning around memory; at 8 GB you stop.

## Who should not buy Evoxt Osaka

You need a China Telecom premium route. Pay BandwagonHost $49.99/month and get the CN2 GIA path. Evoxt does not sell it for Osaka.

You need a managed panel. Every Evoxt plan here is self-managed, and no control-panel license is bundled.

You need a published SLA, a documented refund window, or a stated IPv6 allocation before you pay. None of those appear on the pricing page.

You need guaranteed stock this afternoon. The Osaka/Hong Kong Premium tier is the constrained one; check the region is selectable in the cart before entering card details.

## FAQ

**Is $2.99 the real monthly price?** Yes, for VM-0.5 with 512 MB RAM, 5 GB SSD and 250 GB of Osaka transfer. There is no separate annual rate published, so monthly billing costs the same per month.

**Does paying yearly save money with Evoxt?** No annual discount is listed on the pricing page. Evoxt instead supports prepaid account credit and terms up to three years, which is a cash-flow option rather than a discount.

**Can I upgrade without migrating?** Yes. Evoxt lets you add individual resources to an existing VM instead of moving to a new plan, so a RAM or CPU bump does not require rebuilding the server.

**Is 500 GB of transfer enough?** It works out to about 16 GB a day. Fine for a text-and-image site, tight if you push daily backups off-site or serve video. Size up to VM-2 for 1,000 GB rather than watching the counter.

**Will my Chinese visitors get low latency?** Some will, but Evoxt publishes no carrier-level routing for Osaka, so you cannot know in advance. Run a month on VM-1 and measure before you plan around it.

## How to decide

512 MB test box or a network endpoint → VM-0.5 at $2.99. One site, one bot, one stack → VM-1 at $5.99. Compiling or multi-threaded work → VM-1.5 at $6.95. Several sites with a live database → VM-2 at $11.99. China Telecom audience where routing is the product → none of these, and budget $49.99/month elsewhere.

Before you pay, do two things: confirm Osaka is selectable in the cart for the plan you picked, and read the invoice preview to see the recurring amount rather than trusting a first-term figure. Those two checks take a minute and settle the questions the pricing table cannot answer.

👉 [Start with the $5.99 Osaka plan and verify the renewal price at checkout](https://bit.ly/EvoXt)
