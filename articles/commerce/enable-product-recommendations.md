---
title: 製品推奨事項の有効化
description: このトピックでは、Microsoft Dynamics 365 Commerce の顧客が使用できる人為的知能の機械学習 (AI-ML) に基づいた製品推奨事項を作成する方法について説明します。
author: bebeale
manager: AnnBe
ms.date: 10/1/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail, eCommerce
ms.author: bebeale
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 2d3f1bc2526eeacb4bd6338a0679eadd95a75989
ms.sourcegitcommit: b5ecde955a69f577de46e7db10e89caaedeb2b49
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/04/2020
ms.locfileid: "3024959"
---
# <a name="enable-product-recommendations"></a>製品推奨事項の有効化

[!include [banner](includes/banner.md)]

このトピックでは、Microsoft Dynamics 365 Commerce の顧客が使用できる人為的知能の機械学習 (AI-ML) に基づいた製品推奨事項を作成する方法について説明します。 製品推奨事項一覧の詳細については、[製品推奨事項の概要](product-recommendations.md) を参照してください。

## <a name="recommendations-pre-check"></a>推奨事項のプレチェック

有効にする前に、製品の推奨事項は、Azure Data Lake Storage (ADLS) を使用するようにストレージを移行した Commerce の顧客に対してのみサポートされていることに注意してください。 

ADLS を有効にする手順については、[Dynamics 365 環境で ADLS を有効にする方法](enable-ADLS-environment.md) を参照してください。

さらに、RetailSale の測定が有効になっていることを確認します。 この設定プロセスの詳細については、[こちら](https://docs.microsoft.com/en-us/dynamics365/ai/customer-insights/pm-measures) を参照してください。


## <a name="turn-on-recommendations"></a>推奨事項を有効にする

製品推奨事項を有効にするには、次の手順を実行します。

1. **Retail と Commerce &gt; 製品推奨事項 &gt; 推奨パラメーター**に移動します。
1. 共有パラメーターのリストで、**推奨リスト**を選択します。
1. **推奨事項を有効にする**のオプションを、**はい** に設定します。

![製品推奨事項の有効化](./media/enableproductrecommendations.png)

> [!NOTE]
> この手順では、製品推奨リストを生成するプロセスを開始します。 リストが有効になり、販売時点管理 (POS) または Dynamics 365 Commerce で表示できるようになるまでに、最大数時間かかる場合があります。

## <a name="configure-recommendation-list-parameters"></a>推奨リスト パラメーターのコンフィギュレーション

既定では、AI-ML ベースの製品推奨リストは推奨値を提供します。 業務の流れに合わせて、既定の推奨値を変更できます。 既定のパラメーターを変更する方法の詳細については、[AI-ML ベースの製品推奨事項結果の管理](modify-product-recommendation-results.md)を参照してください。

## <a name="show-recommendations-on-pos-devices"></a>POS デバイスの推奨事項を表示する

Commerce バック オフィスで推奨事項を有効にした後、レイアウト ツールを使用して、推奨事項パネルをコントロール POS 画面に追加する必要があります。 このプロセスの詳細については、[POS デバイスのトランザクション画面への推奨設定コントロールの追加](add-recommendations-control-pos-screen.md) を参照してください。 

## <a name="enable-personalized-recommendations"></a>パーソナライズされた推奨事項の有効化

パーソナライズされた推奨事項を受信する方法の詳細については、[パーソナライズされた推奨事項の有効化](personalized-recommendations.md) を参照してください。

## <a name="additional-resources"></a>追加リソース

[製品推奨事項の概要](product-recommendations.md)

[パーソナライズされた推奨事項の有効化](personalized-recommendations.md)

[ページへの製品推奨リストの追加](add-reco-list-to-page.md)

[POS デバイスへの推奨事項パネルの追加](add-recommendations-control-pos-screen.md)

[製品収集モジュールの概要](product-collection-module-overview.md)

[Dynamics 365 環境での ADLS の有効化](enable-ADLS-environment.md)

