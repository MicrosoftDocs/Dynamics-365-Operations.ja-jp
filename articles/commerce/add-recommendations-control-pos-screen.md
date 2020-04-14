---
title: トランザクション画面への推奨設定の追加
description: このトピックでは、Microsoft Dynamics 365 Commerce の画面レイアウト デザイナーを使用して販売時点管理 (POS) デバイスのトランザクション画面にレコメンデーション コントロールを追加する方法について説明します。
author: bebeale
manager: AnnBe
ms.date: 03/19/20
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: RetailStoreTable, RetailTillLayout
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 260624
ms.assetid: a4f9d315-9951-451c-8ee6-37f9b3b15ef0
ms.search.region: global
ms.search.industry: Retail
ms.author: asharchw
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: a39389da0908953cbbc161f07d067ce3fc569a1b
ms.sourcegitcommit: de5af1912201dd70aa85fdcad0b184c42405802e
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/21/2020
ms.locfileid: "3154135"
---
# <a name="add-recommendations-to-the-transaction-screen"></a>トランザクション画面への推奨設定の追加

[!include [banner](includes/banner.md)]


このトピックでは、Microsoft Dynamics 365 Commerce の画面レイアウト デザイナーを使用して販売時点管理 (POS) デバイスのトランザクション画面にレコメンデーション コントロールを追加する方法について説明します。 製品推奨事項の詳細については、[POS ドキュメントの製品推奨事項](product.md)を参照してください。


Commerce を使用するときに、POS デバイスに製品レコメンデーションを表示できます。 製品レコメンデーションを表示するには、画面レイアウト デザイナーを使用してトランザクション画面にコントロールを追加する必要があります。 

## <a name="open-layout-designer"></a>レイアウト デザイナーを開く

1. **Retail と Commerce** &gt; **チャネル設定** &gt; **POS 設定** &gt; **POS** &gt; **画面レイアウト**の順に移動します。
2. クイック フィルターを使用して、コントロールを追加する画面を検索します。 たとえば、**F2CP16:9M** の値を使用して**画面レイアウト ID** フィールドをフィルター処理します。
3. 一覧で、目的のレコードを見つけ、選択します。 たとえば、**名前: F2CP16:9M 画面レイアウト ID: F2CP16:9M** を選択します。
4. **レイアウト デザイナー**をクリックします。
5. プロンプトに従ってレイアウト デザイナーを起動します。 資格情報を求められたら、レイアウト デザイナーを**画面レイアウト**ページから起動した際に使用していたものと同じ資格情報を入力します。
6. ログインすると、以下のものに類似したページが表示されます。 レイアウトは、店舗に対して行われたカスタマイズによって異なります。


    [![レイアウト デザイナー](./media/screenlayout-pic-1.png)](./media/screenlayout-pic-1.png)

## <a name="choose-a-display-option"></a>表示オプションを選択

使用できる 2 つのコンフィギュレーション オプションがあります。 店舗に最も合っているオプションを選択し、残りの手順にに従ってコントロールのセットアップを完了します。 2 つのオプションは次のとおりです。

- レコメンデーションは常に表示できます。
- **レコメンデーション**タブが画面の右側のグリッドに表示されます。

### <a name="make-recommendations-always-visible"></a>レコメンデーションを常に表示する


1. 左側が顧客パネルと同じ高さになるように、トランザクション明細行の詳細領域の高さを下げます。


    [![トランザクション明細行の詳細領域の高さを減少](./media/screenlayout-pic-2.png)](./media/screenlayout-pic-2.png)

2. 左側のメニューから、トランザクション明細行の詳細領域とトランザクション画面の中央下にあるボタン グリッドの間にレコメンデーション コントロールをドラッグ アンド ドロップします。 そのスペースに合うようにコントロールのサイズを変更します。

    [![レイアウトに追加されたレコメンデーション コントロール](./media/screenlayout-pic-3.png)](./media/screenlayout-pic-3.png)


3. **X** をクリックして、レイアウト デザイナーを保存して終了します。
4. Commerce で、**Retail と Commerce** &gt; **Retail と Commerce IT** &gt; **配布スケジュール**の順に移動します。
5. ボックスの一覧で、**1090 レジスター**を選択します。
6. **今すぐ実行**をクリックします。


### <a name="add-a-recommendations-tab-to-the-button-grid-on-the-right-side-of-the-screen"></a>画面の右側のボタン グリッドにレコメンデーション タブを追加する

1. ページの右側にあるボタン グリッドで最後のタブの下にある空いている場所を右クリックします。

2. **カスタマイズ**をクリックします。

    [![カスタマイズ - タブコントロール ダイアログ ボックス](./media/pic-5.png)](./media/pic-5.png)

3. **新しいタブ**をクリックします。
4. さっき追加した新しいタブを探します。 スクロール ダウンしなければならない場合があります。
5. **コンテンツ**のドロップダウンで、**お勧めの製品**を選択します。

    [![コンテンツ フィールドのお勧め製品を選択](./media/pic-6.png)](./media/pic-6.png)

6. **ラベル**フィールドに、このレコメンデーション タブの名前を入力します。たとえば、「お勧めの製品」と入力します。
7. **画像**フィールドで、タブで表示する画像を選択します。
8. **OK**をクリックします。 新しいタブがボタン グリッドに表示されます。
9. **X** をクリックして、レイアウト デザイナーを保存して終了します。
10. Commerce で、**Retail と Commerce** &gt; **Retail と Commerce IT** &gt; **配布スケジュール**の順に移動します。
11. ボックスの一覧で、**1090 レジスター**を選択します。
12. **今すぐ実行**をクリックします。

## <a name="additional-resources"></a>追加リソース

[製品推奨事項の概要](product-recommendations.md)

[Dynamics 365 Commerce 環境での ADLS の有効化](enable-adls-environment.md)

[製品推奨事項の有効化](enable-product-recommendations.md)

[カスタマイズされた推奨事項を有効にする](personalized-recommendations.md)

[カスタマイズされた製品推奨事項のオプト アウト](personalization-gdpr.md)

[POS での製品推奨事項の追加](product.md)

[AI-ML 推奨事項結果の調整](modify-product-recommendation-results.md)

[収集された推奨事項の手動作成](create-editorial-recommendation-lists.md)

[推奨事項とデモ データの作成](product-recommendations-demo-data.md)

[製品推奨事項に関するよく寄せられる質問](faq-recommendations.md)
