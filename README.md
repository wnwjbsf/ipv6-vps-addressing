# IPv6 VPS: One Address or a Whole /64, Does Dual-Stack Cost Extra, and What JustHost.asia’s $1.60 IPv6-Only Line Actually Includes

JustHost.asia sells three separate VPS families, and each one answers the “IPv6 VPS” question differently. The **IPv6-only KVM line starts at $1.60/mo** on 12-month billing, the **dual-stack IPv4+IPv6 line starts at $2.60/mo**, and the main NVMe line starts at **$1.99/mo**. What none of the price pages state outright is how many IPv6 addresses each plan carries, whether the prefix is a /128 or a /64, and whether IPv6 is live in the particular location you select at checkout.

Those three unknowns decide whether a $1.60 box is a bargain or a support ticket. So the plan list and prices come first, then the part most comparison pages skip: what different hosts mean by “IPv6 VPS”, the /128 gateway problem, and the cloud-init setting that wipes your network config on reboot.

> **Quick pick:** if you need a box that speaks IPv6 and little else, JustHost.asia’s IPv6-only line at **$1.60/mo** (12-month billing) is the cheapest entry point on the price list. If you need both stacks on one machine, **HDD VPS Start at $2.60/mo** annual gets you 1 vCPU, 512 MB RAM and 5 GB disk with IPv4 and IPv6 addresses. Either way, open a ticket and ask for the prefix size before you pay. 👉 [See JustHost.asia’s current IPv6-only and dual-stack VPS prices](https://justhost.asia/en/vps?ref=196392)

## JustHost.asia VPS plans and prices

The site splits its VPS range into three product lines with three different price bases, so here they are as three tables. All figures are as displayed on the official price pages, in USD. The 12-month column is the per-month rate when you pay for a year up front, not the total.

### Main NVMe line

Every plan below has an unmetered port at the listed fair-share speed, and the traffic figure is the site’s own conversion of that port speed into monthly volume.

| Plan | vCPU / RAM / NVMe | Port (fair-share) | Monthly | 12-month | Order |
| --- | --- | --- | --- | --- | --- |
| VPS Promo | 1 core / 512 MB / 5 GB | 10 Mbps (~4+ TB) | $1.99 | not shown | [Order VPS Promo](https://justhost.asia/en/services/vps/tariffs/promo-c1r512nvme?ref=196392) |
| New Star | 1 core / 1024 MB / 10 GB | 100 Mbps (~31+ TB) | $3.81 | $3.05 | [Order New Star](https://justhost.asia/en/services/vps/tariffs/new-star-c1r1024nvme?ref=196392) |
| Sirius | 1 core / 1024 MB / 20 GB | 300 Mbps (~93+ TB) | $4.85 | $3.88 | [Order Sirius](https://justhost.asia/en/services/vps/tariffs/sirius?ref=196392) |
| Arcturus | 1 core / 2048 MB / 30 GB | 300 Mbps (~93+ TB) | $6.92 | $5.53 | [Order Arcturus](https://justhost.asia/en/services/vps/tariffs/arcturus?ref=196392) |
| Double Star | 2 cores / 2048 MB / 20 GB | 200 Mbps (~62+ TB) | $7.08 | $5.67 | [Order Double Star](https://justhost.asia/en/services/vps/tariffs/double-star-c2r2048nvme?ref=196392) |
| Alpha Centauri | 2 cores / 2048 MB / 40 GB | 400 Mbps (~124+ TB) | $8.99 | $7.19 | [Order Alpha Centauri](https://justhost.asia/en/services/vps/tariffs/alpha_centauri?ref=196392) |
| Bright Star | 4 cores / 4096 MB / 30 GB | 300 Mbps (~93+ TB) | $9.80 | $7.84 | [Order Bright Star](https://justhost.asia/en/services/vps/tariffs/bright-star-c4r4096nvme?ref=196392) |
| Vega | 2 cores / 4096 MB / 80 GB | 500 Mbps (~155+ TB) | $13.44 | $10.75 | [Order Vega](https://justhost.asia/en/services/vps/tariffs/vega?ref=196392) |
| Capella | 4 cores / 4096 MB / 120 GB | 750 Mbps (~232+ TB) | $18.30 | $14.64 | [Order Capella](https://justhost.asia/en/services/vps/tariffs/capella?ref=196392) |

New Star, Double Star and Bright Star require a minimum order of three months. The Promo plan’s 12-month cell is displayed as a dash rather than a price, so treat $1.99 as the number to plan around.

Larger configurations sit above Capella, and several of those sizes appear cheaper in the Special offers list below.

### Special offers (same hardware, lower price)

| Plan | vCPU / RAM / NVMe | Port (fair-share) | Monthly | 12-month | Order |
| --- | --- | --- | --- | --- | --- |
| Sirius Special | 1 core / 1024 MB / 20 GB | 300 Mbps | $2.81 | $2.25 | [Order Sirius Special](https://justhost.asia/en/vps?ref=196392) |
| Arcturus Special | 1 core / 2048 MB / 30 GB | 300 Mbps | $4.01 | $3.21 | [Order Arcturus Special](https://justhost.asia/en/vps?ref=196392) |
| Vega Special | 2 cores / 4096 MB / 80 GB | 500 Mbps | $7.79 | $6.23 | [Order Vega Special](https://justhost.asia/en/vps?ref=196392) |
| Yildun Special | 4 cores / 8192 MB / 200 GB | 750 Mbps | $16.20 | $12.96 | [Order Yildun Special](https://justhost.asia/en/vps?ref=196392) |
| Betelgeuse Special | 6 cores / 12288 MB / 400 GB | 750 Mbps | $26.40 | $21.12 | [Order Betelgeuse Special](https://justhost.asia/en/vps?ref=196392) |
| Altair Special | 8 cores / 24576 MB / 600 GB | 750 Mbps | $47.40 | $37.92 | [Order Altair Special](https://justhost.asia/en/vps?ref=196392) |

Compare rows before you pick a side: Sirius Special and regular Sirius are the same 1 core / 1 GB / 20 GB / 300 Mbps machine, and the Special costs **$2.25/mo annual against $3.88**. Arcturus is $5.53 annual, Arcturus Special $3.21. Check the Special offers list first; when stock exists, there is no reason to pay the regular rate.

### IPv4 + IPv6 line (storage chosen at checkout)

| Plan | vCPU / RAM / Disk | Storage type | Monthly | 12-month | Order |
| --- | --- | --- | --- | --- | --- |
| HDD VPS Start | 1 core / 512 MB / 5 GB | HDD | $3.25 | $2.60 | [Order HDD VPS Start](https://justhost.asia/en/vps?ref=196392) |
| SSD VPS Start+ | 1 core / 512 MB / 5 GB | SSD | $3.90 | $3.12 | [Order SSD VPS Start+](https://justhost.asia/en/vps?ref=196392) |
| NVMe VPS Start++ | 1 core / 512 MB / 5 GB | NVMe | $4.22 | $3.38 | [Order NVMe VPS Start++](https://justhost.asia/en/vps?ref=196392) |
| HDD VPS Standard | 2 cores / 2048 MB / 25 GB | HDD | $11.00 | $8.80 | [Order HDD VPS Standard](https://justhost.asia/en/vps?ref=196392) |
| SSD VPS Standard+ | 2 cores / 2048 MB / 25 GB | SSD | $13.20 | $10.56 | [Order SSD VPS Standard+](https://justhost.asia/en/vps?ref=196392) |
| NVMe VPS Standard++ | 2 cores / 2048 MB / 25 GB | NVMe | $14.30 | $11.44 | [Order NVMe VPS Standard++](https://justhost.asia/en/vps?ref=196392) |
| HDD VPS Super | 4 cores / 4096 MB / 50 GB | HDD | $22.00 | $17.60 | [Order HDD VPS Super](https://justhost.asia/en/vps?ref=196392) |
| SSD VPS Super+ | 4 cores / 4096 MB / 50 GB | SSD | $26.40 | $21.12 | [Order SSD VPS Super+](https://justhost.asia/en/vps?ref=196392) |
| NVMe VPS Super++ | 4 cores / 4096 MB / 50 GB | NVMe | $28.60 | $22.88 | [Order NVMe VPS Super++](https://justhost.asia/en/vps?ref=196392) |

This line is priced above the main NVMe line for comparable hardware: **2 cores / 2 GB / 25 GB NVMe here costs $14.30 monthly, while Double Star with 2 cores / 2 GB / 20 GB NVMe costs $7.08**. Either the dual-stack list carries something the cheaper plans don’t, or it is simply a higher-margin SKU. Support can tell you which, and it is worth one message before you pay double.

The IPv6-only line is quoted on the same page as **“IPv6 address only”, KVM, storage type selectable at checkout, from $1.60/mo** on annual billing. Treat that $1.60 as the cheapest configuration in the family, the same way $2.60 maps to HDD VPS Start on the dual-stack side.

One more thing to settle before ordering. The company’s own profile states that all plans include IPv4/IPv6, but the price list keeps a separate IPv6-only category, and a published review of the São Paulo location reports that IPv6 is not supported there. Availability clearly varies by plan and by data centre, so confirm both for the specific location you pick. 👉 [Check the plan and location you’re considering](https://justhost.asia/en/vps?ref=196392)

## What “IPv6 VPS” means at three different hosts

This is the part that decides whether you spend ten minutes or a whole evening on setup. The same three-word phrase covers three quite different products.

**1. One address, delivered but not configured.** OVHcloud documents this model plainly: every VPS ships with one IPv4 and one IPv6 address, but only IPv4 is configured by default, and IPv6 has to be set up manually on your system. You pull three values from the control panel (address, prefix, gateway) and then edit a different file depending on the OS: `/etc/network/interfaces` on Debian 11, Netplan YAML under `/etc/netplan/` on Debian 12 and Ubuntu 22.04 or later, `ifcfg-eth0` on Rocky Linux and AlmaLinux 8/9, NetworkManager `.nmconnection` files on version 10, or the adapter properties on Windows Server. OVHcloud also notes that recent Linux images often arrive with IPv6 already configured, so check the existing config file before touching anything.

**2. A separate interface you switch on in a panel.** ServerPoint takes the opposite approach: three interfaces per VPS, with public IPv4 on eth0, a private VLAN on eth1, and IPv6 on a dedicated eth2. IPv6 is off by default and turned on from the client portal, with no editing of `/etc/network/interfaces` at all. Its announcement states that a **/64 block is included with every VPS at no extra cost**, with /56 blocks available for more addresses, live in Silicon Valley, Amsterdam and Singapore, and still rolling out in Las Vegas, Dallas and Ashburn. Older instances need a single reboot so their automation can attach the interface.

**3. IPv6 only, no IPv4 at all.** This is JustHost.asia’s $1.60 line, and it is a genuinely different product rather than a discount. There is no IPv4 address to fall back on: your SSH session, your monitoring, your package mirrors and your DNS all have to work over IPv6 from wherever you are connecting. That is fine on a dual-stack home connection and painful on a mobile network or office link without IPv6.

A fourth variant exists too: Liquid Web’s IPv6 page, dated February 2025, adds IPv6 free to any VPS if you tick “Add IPv6” while building the server, which puts the choice in the order form rather than in the OS.

Before paying anyone, get four answers in writing: how many addresses, what prefix (/128, /64, /56), is it on by default, and does enabling it mean editing files or clicking a toggle. The prefix matters most. A /128 is one address. A /64 is 18,446,744,073,709,551,616 addresses, which is what you need for containers, a proxy pool, or dozens of sites each wanting its own address.

## Two things that will eat an evening: the /128 gateway and cloud-init

Both come straight out of OVHcloud’s own troubleshooting notes, and both hit people who did everything else right.

**The gateway that isn’t in your subnet.** With a /128 prefix you have exactly one address and the gateway sits outside your subnet, so the OS or the Windows dialog complains that the gateway is not on the same subnet. The fix documented by OVHcloud is to change the prefix from /128 to /64, which pulls the gateway into your subnet. Restarting the network service may not be enough; a full reboot finalises it. On Windows, also check that the firewall allows ICMPv6, or the address will look dead when it isn’t.

**Cloud-init resetting your network config on boot.** Cloud-init is installed by default on most VPS images, and on newer distributions (CentOS, Debian 9, Ubuntu 16.x and later) it can reset the network configuration at startup, quietly undoing the file you just edited. The documented workaround is to create `/etc/cloud/cloud.cfg.d/98-disable-network-config.cfg` containing:


network: {config: disabled}


Delete that file to hand network management back to cloud-init. A reboot may be needed for the change to take effect.

Two smaller checks save time. If you want to test an address before committing to a config file, add it temporarily with `ip addr add YOUR_IPv6/PREFIX dev eth0` and `ip -6 route add default via YOUR_GATEWAY dev eth0`; a reboot clears it. And run `ip addr` first to confirm the interface name, because some VPS instances ship with two NICs and the IPv6 address belongs on `eth1`, not `eth0`.

## Which JustHost.asia plan fits your job

**A single site that just needs to be reachable over IPv6.** Sirius Special at **$2.25/mo** on 12-month billing is the sensible floor: 1 core, 1 GB RAM, 20 GB NVMe, 300 Mbps fair-share port. Skip the $1.99 Promo unless you are genuinely fine with 512 MB RAM, 5 GB of disk and a 10 Mbps port, which is tight for a control panel plus a database.

**Both stacks, one machine, cheap.** HDD VPS Start at **$2.60/mo** annual is the cheapest dual-stack entry, but 5 GB of HDD is small. If the workload is real, the main NVMe line at $3.05–$3.88 gives you NVMe for less than the dual-stack SSD equivalents.

**Bulk addresses: containers, proxies, many sites.** This is where you must not guess. Ask support whether the IPv6-only line hands out a /64 or a single /128, because a /128 is useless for a container fleet. If the answer is /64, $1.60/mo is an unusually low price for that. 👉 [Start with JustHost.asia’s IPv6-only VPS line](https://justhost.asia/en/vps?ref=196392)

**You don’t want to touch config files.** JustHost.asia doesn’t advertise a panel toggle for IPv6, so assume you may be editing Netplan or `ifcfg-eth0` yourself. If that is a hard no, a host with a portal switch is the better fit even at a higher price.

**Users in mainland China or Brazil.** The company advertises CN2 connectivity and 45 locations, and third-party reviews of the São Paulo location describe one-click data-centre switching and one-click IP switching with up to 50 switches per VM. The same review reports that IPv6 is not supported in Brazil, which is exactly why location-by-location confirmation matters.

## Support and stability: what buyers report

The public Trustpilot page for JustHost.Asia carries complaints worth reading before you commit anything important: live chat described as an unhelpful bot, a full outage on 2 March 2026 with roughly 15 hours of silence, error 305 loops requiring repeated reboots, and support replies quoted at up to 48 hours. Cheap IPv6 test boxes and throwaway proxy nodes survive that. Production sites with uptime commitments do not. Payments accepted include crypto, credit cards, PayPal, Alipay and UnionPay, and the price pages don’t state a refund period, so ask about it in the same ticket as the prefix question.

## FAQ

**Is JustHost.asia’s IPv6 a /128 or a /64?**
The price pages don’t say. The IPv6-only line is described as “IPv6 address only”, which tells you there is no IPv4, not how large the allocation is. Ask before ordering.

**Is IPv6 on by default?**
Unconfirmed. The company states all plans include IPv4/IPv6, but a published review of the São Paulo location says IPv6 isn’t supported there, so it varies. OVHcloud’s default of delivering IPv6 unconfigured shows why you shouldn’t assume it works out of the box anywhere.

**Does adding IPv6 cost extra?**
No IPv6 surcharge appears anywhere on the price list. The IPv6-only line is the cheapest product JustHost.asia sells at $1.60/mo annual, and the dual-stack line is priced by hardware rather than by address family.

**Will I have to reconfigure IPv6 after reinstalling the OS?**
Possibly, and cloud-init can also reset your configuration on reboot even without a reinstall. Keep the file at `/etc/cloud/cloud.cfg.d/98-disable-network-config.cfg` in mind if settings keep disappearing.

**Can I add an IPv4 address to an IPv6-only VPS later?**
Not stated on the site. If you might need IPv4 fallback, buy the dual-stack line and skip the question.

## Before you order

Match the line to the job: IPv6-only at **$1.60/mo** for IPv6-native workloads where you can confirm the prefix is a /64; dual-stack at **$2.60/mo** if you need IPv4 reachability for visitors, monitoring or your own SSH access; Sirius Special at **$2.25/mo** if you just want one well-specced box with an IPv6 address on it.

Then send two questions to support in one ticket: what prefix comes with the plan, and is IPv6 enabled in the location I’m ordering. The answers change which product you should buy, and they’re free to ask. 👉 [Compare JustHost.asia’s IPv6-only and dual-stack VPS plans](https://justhost.asia/en/vps?ref=196392)
