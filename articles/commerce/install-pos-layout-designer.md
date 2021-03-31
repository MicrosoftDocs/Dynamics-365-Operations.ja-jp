---
title: POS レイアウト デザイナーのインストール
description: ワンクリック デザイナーを使用して、ランドスケープ モード、ポートレート モード、店舗、レジスター、レジ担当者、マネージャ用など、異なる Modern POS (MPOS) やクラウド POS のレイアウトを作成することができます。
author: athinesh99
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: RetailTillLayout
audience: Application User
ms.reviewer: josaw
ms.custom: 219684
ms.assetid: 2e2c4eea-c6e2-4912-9832-a6b22416e39f
ms.search.region: Global
ms.search.industry: Retail
ms.author: athinesh
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: d96343e4258c84988a675599ab35d93f18ab36b9
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/15/2021
ms.locfileid: "5213141"
---
# <a name="install-the-pos-layout-designer"></a>POS レイアウト デザイナーのインストール

[!include [banner](includes/banner.md)]

ワンクリック デザイナーを使用して、ランドスケープ モード、ポートレート モード、店舗、レジスター、レジ担当者、マネージャ用など、異なる Modern POS (MPOS) やクラウド POS のレイアウトを作成することができます。

MPOS、またはクラウド POS のグラフィカル デザイン インターフェイスは、レジ レイアウトによって制御されます。 レイアウトによって、さまざまなオブジェクトの位置が制御されます。 たとえば、合計のレイアウト、品目グリッド レイアウト、顧客のレイアウト、支払のレイアウト、各種メニュー ボタンのレイアウトがあります。 また、レイアウトには、作業者に対して表示される販売インターフェイスの全体的な外観も含まれます。

## <a name="install-the-one-click-designer"></a>ワンクリック デザイナーをインストールする

1. Commerce では、左上のメニューを使って、**Retail および Commerce** &gt; **チャネル設定** &gt; **POS 設定** &gt; **POS** &gt; **画面レイアウト** の順に移動します。
2. **Windows のモダン POS** または **クラウド POS** のアプリケーション タイプを持つレイアウトを選択し、**レイアウト デザイナー** をクリックします。
3. ワンクリック デザイナーをインストールする場合、Internet Explorer ウィンドウの下部に表示される通知バーの **開始** をクリックします。 (通知バーは、他のブラウザでは別の場所に表示される場合があります。)
4. 表示される **アプリケーションの実行 - セキュリティの警告** メッセージ ボックスで、**実行** をクリックし、Retail デザイナー ホストをインストールします。 インストールの進捗状況を進捗状況インジケータが表示します。
5. インストールが完了したら、**サインイン** ページで Commerce のユーザー名とパスワードを入力し、**サインイン** をクリックしてデザイナーを開始します。
6. ログイン情報が認証されデザイナーを開始した後に、独自のレイアウトを作成するか、または既存のレイアウトを変更することができます。

    [![ワンクリック デザイナーでレイアウトする](./media/screenlayoutdesign_mposdownload-1024x664.png)](./media/screenlayoutdesign_mposdownload.png)

## <a name="troubleshoot-the-installation-of-the-layout-designer"></a>レイアウト デザイナーのインストールに関するトラブルシューティング

- **デザイナー** をクリックしても、インストーラーをダウンロード (または実行) するプロンプトが表示されません、または現在のセキュリティ設定によりファイルがダウンロードできません。 

    **ソリューション**

    - Internet Explorer で、ポップアップ ブロックがこのサイトに対して無効であることを確認します。 **設定** &gt; **オプション** &gt; **プライバシー** &gt; **ポップアップ ブロッカーを探す** をクリックし、変更が必要な場合は設定を変更します。
    - Internet Explorer で、Commerce の URL を信頼済みサイトに追加します。 **設定** &gt; **オプション** &gt; **セキュリティ** &gt; **信頼済みサイト** &gt; **サイト** &gt; **追加** をクリックします。

- プログラムが起動せず、仕入先に連絡するように指示されます。

    **ソリューション:** Internet Explorer で、Commerce の URL を信頼済みサイトに追加します。 **設定** &gt; **オプション** &gt; **セキュリティ** &gt; **信頼済みサイト** &gt; **サイト** &gt; **追加** をクリックします。

**既知の問題:** Google Chrome と Mozilla Firefox ブラウザーでデザイナーが正しく作動しません。 問題を修正中です。

## <a name="additional-resources"></a>追加リソース

[コンフィギュレーション、インストール、および有効化 Retail Modern POS (MPOS)](retail-modern-pos-device-activation.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]