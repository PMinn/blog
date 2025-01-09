---
layout: post
title: 在 Linux 登入 github
tags: [linux,git]
---

1. 進入.ssh資料夾
`cd ~/.ssh`

2. 產生鑰匙
`ssh-keygen`

3. 複製.pub內容
`cat id_rsa.pub`

4. 將密鑰新增至github (Settings -> SSH and GPG keys -> New SSH key -> select Auth. Key and past Key)