---
title: Invoice Capture ソリューションの概要
description: この記事では、Invoice Capture ソリューションについて解説します。
author: sunfzam
ms.date: 09/25/2022
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: VendorInvoiceWorkspace, VendInvoiceInfoListPage
audience: Application User
ms.reviewer: twheeloc
ms.custom:
- "13971"
- intro-internal
ms.assetid: 0ec4dbc0-2eeb-423b-8592-4b5d37e559d3
ms.search.region: Global
ms.author: zezhangzhao
ms.search.validFrom: 2022-09-28
ms.dyn365.ops.version: ''
ms.openlocfilehash: 76441220b93744527f412110db536601a2fa1dd9
ms.sourcegitcommit: 40c80a617b903c2b26e44b41147e0021c5cb680d
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/18/2022
ms.locfileid: "9691213"
---
# <a name="invoice-capture-solution"></a>Invoice Capture ソリューション

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

この記事では、デジタル請求書画像から仕入先請求書を自動作成する Invoice capture ソリューションについて解説します。

買掛金勘定 (AP) 部門は、入庫した商品およびサービスの請求書を管理および処理します。 AP 担当は、次の理由から仕入先請求書のデータを検証します:

- 決算時に調整や修正が必要な場合、余分な手間を省く
- 仕入先請求書に対して時間的な支払を行い、誤りや問題による財務上の損失を回避する

光学式文字認識 (OCR) は、過去数年間でさまざまな業界で広く使用されるようになりました。 印刷されたテキストは電子化され、電子的な編集、検索、よりコンパクトな保存、オンライン上での表示が可能になっています。 デジタル テキストは、コンピュータ、機械翻訳、テキストから変更、主要データ、テキスト マイニングなどの機械プロセスで使用できます。

人工知能 (AI) 技術の進化により、最新の OCR ソリューションでは、さまざまなベンダーのさまざまな請求書フォーマットを、人手をかけずに読み取ることができるようになりました。 請求書を手作業で処理するのではなく、自動化することによって労力を削減し、精度の向上を図ることができると認識する企業が増えています。

## <a name="system-landscape"></a>システム ランドスケープ

次の図は、Invoice Capture ソリューションの主要なコンポーネントと手順を示しています。

[![Invoice Capture ソリューションのコンポーネントと手順。](./media/Invoice-capture2.png)](./media/Invoice-capture2.png)

## <a name="required-roles"></a>必須のロール

次の表に、Invoice Capture ソリューションの設定と使用に必要となるロールを示します。

| ロール          | アクション | システム | ロールの名称 |
|---------------|---------|---------|-----------|
| 管理者 | <ul><li>Microsoft Power Platform で環境を設定します。</li><li>Microsoft Power Platform でソリューションを展開します。</li><li>Dynamics 365 と AI Builder の接続を設定します。</li><li>Azure Data Lake Storage の場所を設定します。</li></ul> | <ul><li>Dynamics 365</li><li>Microsoft Power Platform</li><li>Azure Data Lake Storage</li></ul> | <ul><li>Dynamics 365 管理者</li><li>Power Platform 管理者</li><li>ストレージ BLOB データの所有者</li></ul> |
| AI メーカー      | <ul><li>フローを管理します。</li><li>カスタムの AI モデルを作成します。</li></ul> | <ul><li>Microsoft Power Platform</li></ul> | <ul><li>シチズン メーカー</li></ul> |
| AP 担当者      | <ul><li>仕入先請求書のステージング領域でアクションを確認し、実行します。</li><ul> | <ul><li>Microsoft Power Platform</li></ul> | <ul><li>Power Platform での新しい AP 担当者ロール</li></ul> |
| AP 担当者      | <ul><li>日次業務を AP 担当者が実行します。</li><li>仕入先請求書ステージング領域に移動します。</li></ul> | <ul><li>Dynamics 365</li></ul> | <ul><li>買掛金勘定係</li></ul> |
  
Invoice Capture のインストールの詳細については、[Invoice Capture のインストール](../accounts-payable/install-invoice-capture.md) を参照してください。  
