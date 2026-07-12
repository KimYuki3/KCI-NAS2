<!-- 日本語 | [English](#kci-nas-english) -->

# KCI-NAS

## 古いパソコンが、最新の NAS に生まれ変わる。

押し入れに眠っている古いパソコン。中古ショップに転がっている数百円のハードディスク。メモリは 8〜16GB。
**しめて 3,000 円 — それだけで、家族の写真も仕事の書類も守る"最新の NAS"を自分で作れます。**

高い専用機は要りません。専門知識も要りません。組んで、電源を入れて、あとは忘れていい。
その間も NAS がディスクの状態を見守り、故障の兆候を早めに知らせ、
ランサムウェアの疑わしい動きを見つけたら共有を守り、パソコンが壊れてもバックアップから元に戻せます。

---

## 他の NAS と何が違うのか

- **既成の商用 NAS は、安いディスクを受け付けないことが多い。**
  KCI-NAS は中古のパソコンと、いちばん安いハードディスクで組めます。
- **高機能な NAS ソフトほど、使いこなすのに知識が要ります。**
  KCI-NAS は、管理画面を開かなくても動くように作っています。
- **多くの NAS は「保存」が中心。**
  KCI-NAS は保存に加えて、**異常を早めに知らせ、守り、戻す**ことに重点を置いています。

## できること

### どの NAS にもある基本機能

- 📁 **ファイル共有** — パソコン・Mac・スマホから読み書き
- 🗄 **RAID** — 複数のディスクを束ねて大容量に。1本壊れても耐えられる
- 🕒 **スナップショット** — 誤って消しても、前の状態に戻せる
- ♻️ **自動バックアップ** — 決めた時間に自動でコピー
- 📱 **リモートアクセス** — 外出先からも
- 🎬 **アプリ追加** — メディアサーバー・防犯カメラ録画・コンテナ など

### KCI-NAS が特に力を入れている機能

- 💽 **安い・SMR ディスクで組める** — SSD キャッシュで速度を補い、いちばん安いディスクを活かす
- ❤️ **壊れる前に知らせる** — ディスクの故障の兆候を、早めに平易な言葉で(交換の目安がわかる)
- 🛡 **ランサムウェア対策** — 疑わしい大量書き換えを検知したら、共有を自動で読み取り専用にして被害の拡大を抑える
- 🔬 **静かな破損を検査** — 気づかぬうちに化けたファイル(ビットロット)を定期的にチェック
- 🔗 **バックアップの無事を確認** — 保存したデータが後から変わっていないことを確かめられる
- 🗑 **確実な消去** — ディスクを手放すとき、本当に消えたことを照合して確認できる
- 🔍 **意味で探す検索** — 書類を日本語・英語で、言葉が少し違っても意味の近いものを探せる
- 😌 **開かない前提の設計** — 管理画面を一度も開かなくても、勝手に守る

## 知っておいてほしいこと

- **速さを競う製品ではありません。** 大切なデータを守ることに重点を置いています。
- **バックアップが前提です。** 大切なデータは必ず複数の場所に保存してください。
- **これは自分で組み立てる自作 NAS です。** 動作や結果を保証するものではありません。ご利用は自己責任でお願いします。

## 動作環境(最低限)

- **CPU** — 64bit(x86_64)、2コア以上。AES-NI 対応だと暗号化が速くなります(2011 年ごろ以降の Intel / AMD ならほぼ対応)
- **メモリ** — 最低 4GB。アプリ(メディアサーバー・コンテナ等)も使うなら 8〜16GB 推奨
- **ディスク** — 1本から使えます。RAID を組むなら 2本以上。SSD を1本足すと動きが軽くなります
- **OS** — Ubuntu Server(x86_64)。画面のいらないサーバー用途なので、デスクトップ版より軽い Server 版がおすすめです

## ⚠️ 免責事項(必ずお読みください)

KCI-NAS は、利用者ご自身が組み立てて運用する **自作 NAS** です。**導入・運用は、すべて個人の責任において行ってください。**

- 本ソフトウェアは「**現状のまま(AS IS)**」提供され、**動作・性能・安全性を一切保証しません。**
- 本ソフトウェアの使用、または使用できなかったことにより生じた **いかなる損害(データの消失・破損、機器の故障、事業上の損失などを含む一切)についても、作者は責任を負いません。**
- **大切なデータは、必ず複数の場所にバックアップしてください。**

インストールを実行した時点で、上記に同意したものとみなします。

## はじめかた

Ubuntu Server のターミナルに、**下の1行を貼り付けて Enter するだけ**:

```bash
curl -sL https://github.com/KimYuki3/KCI-NAS2/releases/latest/download/install.sh | sudo bash
```

終わったら `http://<NASのIP>:8080` を開き、`admin` / `admin` でログイン(**すぐにパスワードを変更**)。

Ubuntu Server の入れ方や、Windows から SSH でつなぐ手順など、くわしくは **[INSTALL.md](INSTALL.md)** を参照してください。

## 質問・要望

ユーザー同士の質問・要望・不具合報告は **[Discussions](../../discussions)** へどうぞ。

## ライセンス

- **個人利用・非商用利用は無償**です。
- **商用利用**(販売・業務での利用・再配布など)には、**別途ライセンス契約が必要**です。お問い合わせください。

(c) Kimura 2026. All rights reserved.

<br>

---
---

<a name="kci-nas-english"></a>

# KCI-NAS (English)

## An old PC, reborn as a modern NAS.

That old computer gathering dust. A used hard drive for a few dollars. 8–16 GB of memory.
**About US$20 of used parts — that's all it takes to build yourself a modern NAS that guards your family photos and work documents.**

No expensive appliance. No expertise required. Assemble it, power it on, and forget it.
Meanwhile the NAS keeps an eye on your disks' health, warns you early of failure signs,
protects your shares if it spots suspicious ransomware-like activity, and lets you restore
from backup even if a PC dies.

---

## How it's different

- **Off-the-shelf commercial NAS often won't accept cheap disks.**
  KCI-NAS runs on a used PC and the cheapest hard drives.
- **The more capable the NAS software, the more expertise it takes.**
  KCI-NAS is built to run without ever opening the admin panel.
- **Most NAS just store.**
  KCI-NAS also **warns early, protects, and restores.**

## What you can do

### Standard features every NAS has

- 📁 **File sharing** — from PC / Mac / phone
- 🗄 **RAID** — pool disks for capacity; survive a single drive failure
- 🕒 **Snapshots** — roll back accidental deletes
- ♻️ **Scheduled backups**
- 📱 **Remote access** — including from outside
- 🎬 **Apps** — media server, camera recording, containers, and more

### What KCI-NAS focuses on

- 💽 **Runs on cheap / SMR disks** — an SSD cache makes up for the speed
- ❤️ **Warns before a disk fails** — early, in plain language (replacement guidance)
- 🛡 **Ransomware protection** — on suspicious mass changes, shares are set read-only to limit damage
- 🔬 **Checks for silent corruption** — periodically scans for bit rot
- 🔗 **Confirms your backups are intact** — verifies stored data hasn't changed later
- 🗑 **Verifiable erase** — when you retire a disk, confirm it was truly wiped
- 🔍 **Meaning-aware search** — find documents in Japanese or English, even when wording differs
- 😌 **Built to protect unattended** — without you ever opening the admin panel

## Good to know

- **Not a product that competes on speed.** It focuses on protecting your data.
- **Backups are assumed.** Always keep copies in more than one place.
- **This is a DIY NAS you build yourself.** No warranty on operation or results. Use at your own risk.

## Requirements (minimum)

- **CPU** — 64-bit (x86_64), 2+ cores. AES-NI recommended for faster encryption (most Intel / AMD since ~2011).
- **Memory** — 4 GB minimum. 8–16 GB recommended if you run apps (media server, containers, etc.).
- **Disks** — works with a single drive. RAID needs 2+. Adding one SSD keeps cheap disks responsive.
- **OS** — Ubuntu Server (x86_64). Since a NAS is headless, the lighter Server edition is recommended over Desktop.

## ⚠️ Disclaimer (please read)

KCI-NAS is a **do-it-yourself NAS that you build and operate yourself. All installation and operation are entirely at your own risk and responsibility.**

- The software is provided **"AS IS", with no warranty** of operation, performance, or safety of any kind.
- **The authors accept no liability for any damage whatsoever** — including data loss or corruption, hardware failure, or business loss — arising from the use of, or inability to use, this software.
- **Always keep backups of important data in more than one place.**

By running the installer, you agree to the above.

## Getting started

Paste **this single line** into your Ubuntu Server terminal and press Enter:

```bash
curl -sL https://github.com/KimYuki3/KCI-NAS2/releases/latest/download/install.sh | sudo bash
```

Then open `http://<NAS-IP>:8080` and log in with `admin` / `admin` (**change the password right away**).

For the full guide (preparing Ubuntu Server, connecting via SSH from Windows), see **[INSTALL.md](INSTALL.md)**.

## Questions & requests

For user questions, requests, and bug reports, please use **[Discussions](../../discussions)**.

## License

- **Personal / non-commercial use is free of charge.**
- **Commercial use** (resale, business use, redistribution, etc.) **requires a separate license agreement.** Please contact us.

(c) Kimura 2026. All rights reserved.
