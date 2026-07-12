<!-- 日本語 | [English](#install-english) -->

# インストール手順

古いパソコンに Ubuntu Server を入れ、いつも使っている Windows パソコンから SSH で接続して設定します。
画面やキーボードを NAS 本体に繋ぎっぱなしにする必要はありません。

> ⚠️ **免責事項**: これは自作 NAS です。**導入・運用はすべて自己責任**で行ってください。本ソフトは無保証で提供され、**データの消失・機器の故障を含むいかなる損害についても作者は責任を負いません**。大切なデータは必ず複数の場所にバックアップしてください。

## 用意するもの

- NAS にする古いパソコン([動作環境](README.md#動作環境最低限)を満たすもの)
- ハードディスク(1本から。RAID を組むなら 2本以上)
- USB メモリ 1本(Ubuntu Server のインストール用、4GB 以上)
- いつも使っている Windows パソコン(設定用)
- 同じルーターに有線 LAN で繋がっていること

## 手順

### 1. Ubuntu Server のインストール USB を作る

1. [Ubuntu Server](https://ubuntu.com/download/server) の ISO をダウンロード(x86_64 / 64bit 版)
2. [Rufus](https://rufus.ie/) などで USB メモリに書き込む

### 2. 古いパソコンに Ubuntu Server を入れる

1. 作った USB を NAS 用パソコンに挿して起動(起動順序で USB を優先)
2. 画面の案内に沿って Ubuntu Server をインストール
3. 途中で **「Install OpenSSH server」にチェック**を入れる(これが後で Windows から繋ぐ鍵)
4. ユーザー名とパスワードを決める(あとで使います)
5. インストールが終わったら USB を抜いて再起動

### 3. NAS の IP アドレスを調べる

NAS 本体で一度だけログインし、次を実行:

```bash
ip -br addr
```

`192.168.x.x` のような番号が NAS の住所です(メモしておく)。
以降は本体に触らなくて済みます。

### 4. Windows から SSH で接続する

Windows 10 / 11 には最初から SSH が入っています。**PowerShell**(または コマンドプロンプト)を開いて:

```powershell
ssh <ユーザー名>@<NASのIP>
# 例: ssh kci@192.168.1.20
```

初回は「本当に接続していいか」と聞かれるので `yes`。パスワードを入れれば接続完了です。

### 5. KCI-NAS をインストールする

SSH でつないだ画面に、下の**1行をコピーして貼り付け、Enter を押すだけ**です:

```bash
curl -sL https://github.com/KimYuki3/KCI-NAS2/releases/latest/download/install.sh | sudo bash
```

あとは「最新版のダウンロード → インストール → 自動起動の設定」まで全部自動で進みます。
しばらく待つと、画面に管理ページの URL が表示されます。

### 6. ブラウザで開く

Windows のブラウザで `http://<NASのIP>:8080` を開きます。
初期パスワードでログインしたら、**必ずパスワードを変更**してください。

これで完了です。あとは画面の案内に沿って、共有フォルダやバックアップを設定できます。

---

> 困ったこと・質問は [Discussions](../../discussions) へどうぞ。

<br>

---
---

<a name="install-english"></a>

# Installation Guide (English)

Install Ubuntu Server on an old PC, then set everything up from your everyday Windows PC over SSH.
You don't need to keep a monitor and keyboard attached to the NAS.

> ⚠️ **Disclaimer**: This is a DIY NAS. **Installation and operation are entirely at your own risk.** The software is provided with no warranty, and **the authors accept no liability for any damage — including data loss or hardware failure**. Always keep backups of important data in more than one place.

## What you need

- An old PC to become the NAS (meeting the [requirements](README.md#requirements-minimum))
- A hard drive (one is enough; RAID needs 2+)
- One USB stick (4 GB+, to install Ubuntu Server)
- Your everyday Windows PC (for setup)
- Both connected to the same router by wired LAN

## Steps

### 1. Make an Ubuntu Server install USB

1. Download the [Ubuntu Server](https://ubuntu.com/download/server) ISO (x86_64 / 64-bit)
2. Write it to the USB stick with a tool such as [Rufus](https://rufus.ie/)

### 2. Install Ubuntu Server on the old PC

1. Boot the NAS PC from the USB (set USB first in the boot order)
2. Follow the on-screen installer
3. **Check "Install OpenSSH server"** during setup — this is what lets you connect from Windows later
4. Choose a username and password (you'll use them soon)
5. When done, remove the USB and reboot

### 3. Find the NAS IP address

Log in once on the NAS itself and run:

```bash
ip -br addr
```

A number like `192.168.x.x` is the NAS's address (note it down).
After this you won't need to touch the machine directly.

### 4. Connect from Windows over SSH

Windows 10 / 11 include SSH out of the box. Open **PowerShell** (or Command Prompt):

```powershell
ssh <username>@<NAS-IP>
# e.g. ssh kci@192.168.1.20
```

Answer `yes` the first time, enter your password, and you're in.

### 5. Install KCI-NAS

Still connected over SSH, just **paste this single line and press Enter**:

```bash
curl -sL https://github.com/KimYuki3/KCI-NAS2/releases/latest/download/install.sh | sudo bash
```

It downloads the latest version, installs it, and sets up auto-start — all automatically.
After a while, the admin page URL is shown on screen.

### 6. Open it in a browser

On Windows, open `http://<NAS-IP>:8080`.
Log in with the initial password, then **change the password immediately**.

That's it. From there, the on-screen guide walks you through shares and backups.

---

> Questions or trouble? Please use [Discussions](../../discussions).
