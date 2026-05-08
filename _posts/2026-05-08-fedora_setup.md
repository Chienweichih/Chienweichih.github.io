---
title: "Fedora 安裝後設定整理"
date: 2026-05-08 23:30:00 +0800
tags: [system]
---

> 本文內容是向 Claude 詢問各項 Fedora 設定問題後，整理記錄而成的筆記。

## 將家目錄資料夾名稱改為英文

安裝 Fedora 時若選擇中文介面，家目錄下的標準資料夾會是中文名稱。執行以下指令可強制改為英文：

```bash
LANG=en_US.UTF-8 xdg-user-dirs-update --force
```

執行完畢後重新登入，若系統詢問是否改回中文，選擇「保留舊名稱」即可。

---

## 系統版本升級

Fedora 的跨版本升級方式請參考官方文件：

[Upgrading Fedora Offline - Fedora Quick Docs](https://docs.fedoraproject.org/en-US/quick-docs/upgrading-fedora-offline)

---

## 更換舊版 Fedora 桌布

可以到以下頁面下載歷年 Fedora 的桌布圖檔，下載後在桌面設定裡手動選擇圖檔即可：

[Fedora Backgrounds Releases - GitHub](https://github.com/fedoradesign/backgrounds/releases)

### 加上 Fedora 浮水印

先確認已安裝 `gnome-shell-extension-background-logo`：

```bash
sudo dnf install gnome-shell-extension-background-logo
```

然後執行以下指令啟用桌布左下角的 Fedora logo 浮水印：

```bash
gsettings set org.fedorahosted.background-logo-extension logo-always-visible true
```

---

## 安裝字體

將字體檔案放到 `~/.local/share/fonts/` 目錄下（若目錄不存在請自行建立），然後執行以下指令更新字體快取：

```bash
fc-cache -fv
```

不需要重開機，系統即可立即認得新字體。

---

## 安裝影片編解碼器

Fedora 預設因授權問題不包含 H.265 等私有編解碼器，導致許多影片無法播放。需要先啟用 RPM Fusion 儲存庫，再安裝相關套件：

```bash
sudo dnf install https://mirrors.rpmfusion.org/free/fedora/rpmfusion-free-release-$(rpm -E %fedora).noarch.rpm
sudo dnf install https://mirrors.rpmfusion.org/nonfree/fedora/rpmfusion-nonfree-release-$(rpm -E %fedora).noarch.rpm
sudo dnf install gstreamer1-libav gstreamer1-plugins-bad-freeworld
sudo dnf install ffmpeg ffmpeg-libs libavcodec-freeworld
sudo dnf install mpv celluloid
```

其中 `mpv` 是功能強大的命令列影片播放器，`celluloid` 則是 mpv 的 GUI 前端。

---

## 筆電省電優化：PowerTop Auto Tune

安裝 PowerTop：

```bash
sudo dnf install powertop
```

建立 systemd service 讓開機時自動套用省電優化，新增 `/etc/systemd/system/powertop.service`，內容如下：

```ini
[Unit]
Description=PowerTop Auto Tune

[Service]
Type=oneshot
ExecStart=/usr/sbin/powertop --auto-tune

[Install]
WantedBy=multi-user.target
```

啟用服務：

```bash
sudo systemctl enable powertop.service
sudo systemctl start powertop.service
```

---

## 安裝中文輸入法

### GNOME

GNOME 環境下直接安裝 `ibus-chewing`，安裝後到「設定 > 鍵盤 > 輸入來源」加入「中文（注音）」即可：

```bash
sudo dnf install ibus-chewing
```

### XFCE

XFCE 環境下建議使用 fcitx5，相容性較好：

```bash
sudo dnf install fcitx5 fcitx5-chewing fcitx5-configtool
```

---

## 推薦應用程式

| 應用程式 | 說明 | 連結 |
|---|---|---|
| Foliate | 電子書閱讀器 | [GitHub](https://github.com/johnfactotum/foliate) |
| TigerVNC | VNC 遠端桌面工具 | [GitHub](https://github.com/TigerVNC/tigervnc) |
| KPatience | 紙牌遊戲（KDE） | [GitHub](https://github.com/KDE/kpat) |
| Skladnik | 推箱子遊戲（KDE） | [GitHub](https://github.com/KDE/skladnik) |
| SuperTuxKart | 開源賽車遊戲 | [GitHub](https://github.com/supertuxkart/stk-code) |
| mGBA | GBA 模擬器 | [GitHub](https://github.com/mgba-emu/mgba) |
| melonDS | Nintendo DS 模擬器 | [GitHub](https://github.com/melonDS-emu/melonDS) |
| DuckStation | PS1 模擬器 | [GitHub](https://github.com/stenzek/duckstation) |
| LocalSend | 跨裝置區域網路檔案傳輸 | [GitHub](https://github.com/localsend/localsend) |
