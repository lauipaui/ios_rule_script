# Rules And Scripts — Fork Guide

[中文](README.md) | **English**

Platform-specific routing rules, rewrites and automation scripts. This is a fork of [blackmatrix7/ios_rule_script](https://github.com/blackmatrix7/ios_rule_script), not a newly authored rule collection. The original Chinese overview, notices, resource links and acknowledgements remain in [README.md](README.md).

## Repository map

| Directory | Contents |
| --- | --- |
| [`rule/`](rule/) | Routing rules grouped by client/platform |
| [`rewrite/`](rewrite/) | Rewrite resources; some need HTTPS interception or script execution |
| [`script/`](script/) | Automation scripts and per-script instructions |
| [`source/`](source/) | Rule sources and supporting material |
| [`external/`](external/) | Third-party resources with their own authors and terms |
| [`icon/`](icon/), [`blank/`](blank/) | Icons and blank/supporting resources |

This is a resource repository, not a single Node application or a universal installer. Choose the README in the relevant client/resource directory. Mihomo/Clash, Surge, Quantumult X, Loon and other formats are not interchangeable.

## Safe use

1. Identify the actual client and supported format.
2. Read the selected resource's documentation and source before importing it.
3. Back up your existing client configuration, then import only the resources you need.
4. Validate with that client, check resource downloads and test representative rules.
5. Restore the backup or use a known-good revision if behavior regresses.

Some rewrites/scripts require MITM or account access. Understand the trust implications before granting those permissions. Never commit real subscriptions, account cookies/tokens or certificate private keys, and do not disable TLS validation to hide download errors.

The default branch is `master`. URLs in upstream documentation still point to **blackmatrix7** and can change independently of this fork. For a pinned fork resource, verify the path at the desired commit before using a URL shaped like:

```text
https://raw.githubusercontent.com/lauipaui/ios_rule_script/COMMIT/PATH
```

Replace the placeholders with a real reviewed commit and file path. Do not blindly rewrite every upstream URL. There is no single test command proving the validity of the entire collection. This documentation update did not import rules, run account scripts or revalidate all external data.

## Script overview from the upstream snapshot

| Script | Description | Framework | Historical status |
| --- | --- | --- | --- |
| [`smzdm`](script/archive/smzdm/) | Shopping tasks and ad-related script | MagicJS 2/3 | Normal |
| [`tieba`](script/tieba/) | Retrying daily sign-in | MagicJS 3 | Normal |
| [`startup`](script/startup/) | Remove cached splash-screen ads | MagicJS 3 | Normal |
| [`manmanbuy`](script/archive/manmanbuy/) | Daily sign-in | MagicJS 2 | Normal |
| [`dingdong`](script/archive/dingdong/) | Daily sign-in | MagicJS 3 | Normal |
| [`famijia`](script/archive/famijia/) | Daily sign-in | MagicJS 2 | Normal |
| [`luka`](script/luka/) | Daily sign-in | MagicJS 2 | Normal |
| [`zheye`](script/zheye/) | Platform-specific script described by upstream | MagicJS 3 | Normal |
| [`synology`](script/archive/synology/) | Download Station resource downloads | MagicJS 3 | Normal |
| [`applestore`](script/applestore/) | Apple Store inventory monitoring | MagicJS 3 | Paused |

Statuses are copied from the snapshot, **not current live-test results**. In this fork, `smzdm`, `manmanbuy`, `dingdong`, `famijia` and `synology` are under `script/archive/`; the historical "Normal" label does not mean they are currently maintained. Selected scripts have Quantumult X Gallery and BoxJS definitions: [`script/gallery.json`](script/gallery.json) and [`script/boxjs.json`](script/boxjs.json). Use the original author for support concerning external resources.

## Upstream notices — English rendering

The authoritative wording is retained in the Chinese README. Its notices state that:

1. Public/social-media accounts and self-media must not republish or distribute the repository's resource files in any form.
2. The principal purpose is learning and studying ES6; legality, accuracy, completeness and effectiveness are not guaranteed.
3. Users or organizations provide their own data and are responsible for its truthfulness, accuracy and legality, as well as the consequences of use.
4. The project has no direct or indirect affiliation with third-party hardware/software; describing use is not an endorsement, and users bear the consequences.
5. Contents are for learning/research and must not be used contrary to applicable national, regional or organizational laws/rules.
6. Third-party modifications are independent acts, and their consequences are not attributable to the upstream project.
7. The upstream asks users to complete learning/research within 24 hours and delete the material, and to develop their own implementation for continuing functional needs.
8. The upstream reserves the right to amend its notices and regards direct/indirect use as acceptance.

This rendering does not change licensing or resolve possible conflicts between notices and licenses. Consult the original author if applicability is unclear.

## Attribution and licensing

Upstream says it collects rather than originates many rules and thanks the authors of the source projects. Root [`LICENSE`](LICENSE) contains **GPL-2.0**; preserve it, upstream notices and directory-specific third-party attribution/terms. This fork does not relicense external resources.

Acknowledgements retained from upstream: [BaileyZyp](https://github.com/BaileyZyp), [Mazeorz](https://github.com/Mazeorz), [LuzMasonj](https://github.com/LuzMasonj), [chouchoui](https://github.com/chouchoui), [ypannnn](https://github.com/ypannnn), [echizenryoma](https://github.com/echizenryoma), [zirawell](https://github.com/zirawell), [urzz](https://github.com/urzz), [ASD-max](https://github.com/ASD-max).
