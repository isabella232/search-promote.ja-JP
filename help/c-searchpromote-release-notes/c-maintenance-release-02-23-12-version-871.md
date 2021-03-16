---
description: Search&amp;Promote 8.7.1リリースノート。
solution: Target
title: Search&amp;Promote 8.7.1リリースノート（2012年2月24日）
topic: リリースノート，サイト検索とマーチャンダイジング
uuid: 3fabf7b2-4a27-4f0a-862a-52f701a0631d
translation-type: tm+mt
source-git-commit: d015154efdccbb4c6a39a56907c0c337ec065c9f
workflow-type: tm+mt
source-wordcount: '179'
ht-degree: 32%

---


# Search&amp;Promote8.7.1リリースノート（2012年2月24日）{#search-promote-release-notes}

## 新機能{#section_CF3326C0E4FD4179A8009FB76D514304}

* [!DNL Search&Promote]内から[!DNL Scene7]アセットにアクセスします。
* [!DNL Scene7]バナーパラメーターを[!DNL Search&Promote]内から設定します。
* ビジネスルールに[!DNL Scene7]バナーを適用します。

[バナーについて](../c-about-design-menu/c-about-banners.md#concept_5BBE01FEC6134393B43CC917C8CC64DA)も参照してください

## 製品機能の強化 {#section_6646341ABC6D428A97F567EDD7090898}

HTC プレゼンテーションテンプレートをメモリおよびファイルの両方にキャッシュできるようになり、検索時のパフォーマンスが向上しました。

## 製品不具合の修正 {#section_6B3602709FB04B3C999C5DFE103CFF7D}

* 新しいユーザー名を追加する際に先頭にスペースを入れておくと、無効なエラーが発生していました。
* サーチクエリに関する問題を修正しました。
* テンプレートファイルキャッシュの無効化を、ガイド付き検索で Apache のリロードが実行されるたびに実行するのではなく、サーバーの起動時にのみ実行するようにしました。
* 「もしかして」機能に関する問題を修正しました。
* xlhtml および ppthtml のクローラー処理に関する問題を修正しました。
* ルールのコピー機能で、名前の値が無意味な文字として表示される。
* テンプレートキャッシュが無効化されないようにタイムスタンプを保持する。
* 「Dynamic Mediaクラシック」バナーダイアログボックスにスクロールバーが表示された場合、一部のパラメーター変更フィールドが切れていた問題を修正しました。
* Dynamic Mediaクラシックバナーパラメーターに対して行ったビジネスルールの変更がすべてステージング領域では動作しましたが、ライブにプッシュした場合は有効になりませんでした。

