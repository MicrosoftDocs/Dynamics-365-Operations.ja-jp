---
title: 小売トランザクションの財務分析コードの編集
description: このトピックでは、Microsoft Dynamics 365 Commerce で小売トランザクションの財務分析コードを編集する方法について説明します。
author: josaw1
ms.date: 11/04/2020
ms.topic: index-page
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ed0f77f7-3609-4330-bebd-ca3134575216
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2018-11-15
ms.dyn365.ops.version: ''
ms.openlocfilehash: d5fee5f5dfee73ddb9fbcf8a33df66c29f9438b49136181633b989d1a02ef4f5
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/05/2021
ms.locfileid: "6765317"
---
# <a name="edit-financial-dimensions-for-retail-transactions"></a>小売トランザクションの財務分析コードの編集

[!include [banner](../includes/banner.md)]

このトピックでは、Microsoft Dynamics 365 Commerce で小売トランザクションの財務分析コードを編集する方法について説明します。

## <a name="edit-financial-dimensions"></a>財務分析コードの編集

Commerce 本社で小売トランザクションの財務分析コードを編集するには、次の手順に従います。

1. **アプリケーション統合用の財務分析コードのコンフィギュレーション** ページを開きます。
1. 有効な **既定の分析コード統合** レコードを選択します。
1. **財務分析コード** クイックタブで、Excel ワークシートで編集するすべての分析コードが、**選択済** リストに表示されていることを確認します。 詳細については、[データ エンティティ](../fin-ops-core/dev-itpro/financial/financial-dimension-configuration-integration.md#data-entities)を参照してください。
1. **明細書** ページ、**小売トランザクション** ページ、または **店舗の財務** ワークスペースの **トランザクションの検証エラー** タイル から Excel ファイルをダウンロードして開きます。
1. トランザクションの財務分析コードを変更するには、**デザイン** を選択し、**トランザクション (監査可能)** 行の横にある鉛筆の記号を選択します。
1. **FinancialDimensionDisplayValue** フィールドを見つけて選択し、Excel ワークシートのヘッダー部分のセルを選択して、**ラベルの追加** を選択します。
1. 前のステップで選択したセルの下のセルを選択し、**値の追加**、**最新の情報に更新** の順に選択します。 財務分析コードが Excel ワークシートに追加され、編集して公開できます。
1. トランザクション明細行の分析コードを変更するには、**販売トランザクション (監査可能)** 行を選択し、鉛筆の記号を選択してから、手順 6 と 7 を繰り返します。
1. 払行明細行の分析コードを変更するには、**支払トランザクション (監査可能)** 行を選択し、鉛筆の記号を選択してから、手順 6 と 7 を繰り返します。

## <a name="additional-resources"></a>追加リソース

[現金売りトランザクションと現金管理トランザクションの編集と監査](edit-cash-trans.md)

[オンライン注文トランザクションと非同期顧客注文トランザクションの編集と監査](edit-order-trans.md)

[小売トランザクションを編集するために Excel ブックを作成する](create-excel-edit.md)

[小売トランザクションを編集するために Excel ブックにフィールドを追加する](add-fields-excel.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]