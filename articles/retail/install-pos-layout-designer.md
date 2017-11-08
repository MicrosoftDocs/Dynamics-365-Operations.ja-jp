---
title: "Retail POS のレイアウト デザイナーをインストールする"
description: "ワンクリック デザイナーを使用して、ランドスケープ モード、ポートレート モード、店舗、レジスター、レジ担当者、マネージャ用など、異なる Retail Modern POS (MPOS) やクラウド POS のレイアウトを作成することができます。"
author: athinesh99
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
ms.search.form: RetailTillLayout
audience: Application User
ms.reviewer: josaw
ms.search.scope: Retail, Operations, Core
ms.custom: 219684
ms.assetid: 2e2c4eea-c6e2-4912-9832-a6b22416e39f
ms.search.region: Global
ms.search.industry: Retail
ms.author: athinesh
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 36c9b70ab16498ec22a7113d0d5debd5de63658a
ms.contentlocale: ja-jp
ms.lasthandoff: 09/29/2017

---

# <a name="install-the-retail-pos-layout-designer"></a>Retail POS のレイアウト デザイナーをインストールする

[!include[banner](includes/banner.md)]


ワンクリック デザイナーを使用して、ランドスケープ モード、ポートレート モード、店舗、レジスター、レジ担当者、マネージャ用など、異なる Retail Modern POS (MPOS) やクラウド POS のレイアウトを作成することができます。

MPOS、またはクラウド POS のグラフィカル デザイン インターフェイスは、レジ レイアウトによって制御されます。 レイアウトによって、さまざまなオブジェクトの位置が制御されます。 たとえば、合計のレイアウト、品目グリッド レイアウト、顧客のレイアウト、支払のレイアウト、各種メニュー ボタンのレイアウトがあります。 また、レイアウトには、作業者に対して表示される販売インターフェイスの全体的な外観も含まれます。

## <a name="install-the-one-click-designer"></a>ワンクリック デザイナーをインストールする
1.  Microsoft Dynamics 365 for Retail では、左上のメニューを使って、[**小売** **とコマース**] &gt; [**チャンネル設定**] &gt; [**POS 設定**] &gt; [**POS**] &gt; [**画面レイアウト**] へ移動します。
2.  **Windows のモダン POS** または**クラウド POS**のアプリケーション タイプを持つレイアウトを選択し、[**レイアウト デザイナー**] をクリックします。
3.  ワンクリック デザイナーをインストールする場合、Internet Explorer ウィンドウの下部に表示される通知バーの [**開始**] をクリックします。 (通知バーは、他のブラウザでは別の場所に表示される場合があります。)
4.  表示される **アプリケーションの実行 - セキュリティの警告** メッセージ ボックスで、[**実行**] をクリックし、Retail デザイナー ホストをインストールします。 インストールの進捗状況を進捗状況インジケータが表示します。
5.  インストール完了後に、デザイナーを開始する場合、**サインイン**ページで Microsoft Dynamics 365 for Retail のユーザー名とパスワードを入力し、[**サインイン** ] をクリックします。
6.  ログイン情報が認証されデザイナーを開始した後に、独自のレイアウトを作成するか、または既存のレイアウトを変更することができます。 [![ワンクリック デザイナーでレイアウトする](./media/screenlayoutdesign_mposdownload-1024x664.png)](./media/screenlayoutdesign_mposdownload.png)

## <a name="troubleshoot-the-installation-of-the-layout-designer"></a>レイアウト デザイナーのインストールに関するトラブルシューティング
-   [**デザイナー**] をクリックしても、インストーラーをダウンロード (または実行) するプロンプトが表示されません、または現在のセキュリティ設定によりファイルがダウンロードできません。 **ソリューション**
    -   Internet Explorer で、ポップアップ ブロックがこのサイトに対して無効であることを確認します。 [**設定**] &gt; [**オプション**] &gt; [**プライバシー**] &gt; [**ポップアップ ブロッカーを探す**] をクリックし、変更が必要な場合は設定を変更します。
    -   Internet Explorerで、Dynamics 365 for Retail の URL を信頼済みサイトへ追加します。 [**設定**] &gt; [**オプション**] &gt; [**セキュリティ**] &gt; [**信頼済みサイト**] &gt; [**サイト**] &gt; [**追加**] をクリックします。
-   プログラムが起動せず、仕入先に連絡するように指示されます。 [**ソリューション:**] Internet Explorer で、Dynamics 365 for Retail の URL を信頼済みサイトへ追加します。 **設定** &gt; **オプション** &gt; **セキュリティ** &gt; **信頼済みサイト** &gt; **サイト** &gt; **追加**をクリックします。

**既知の問題:** Google Chrome と Mozilla Firefox ブラウザでデザイナーが正しく作動しません。 問題を修正中です。

<a name="see-also"></a>参照
--------

[Retail Modern POS の設定、ダウンロード、インストール、および有効化。](retail-modern-pos-device-activation.md)




