---
title: Dynamics 365 for Retail バージョン 10.0.3 の機能をプレビューする
description: このトピックでは Dynamics 365 for Retail のプレビュー中の機能について説明します。
author: josaw1
manager: AnnBe
ms.date: 06/14/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-retail
ms.technology: ''
audience: Developer, IT Pro
ms.reviewer: josaw
ms.search.scope: Operations, Retail
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: josaw
ms.search.validFrom: 2019-04-23
ms.dyn365.ops.version: Release 10
ms.openlocfilehash: 30e1738fdd3ef495b3117745aff85153e629d310
ms.sourcegitcommit: 672c94704e9a2b0ec7ee3c111d4ceb1bb8597969
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/14/2019
ms.locfileid: "1632042"
---
# <a name="whats-new-or-changed-in-dynamics-365-for-retail-version-1003"></a>Dynamics 365 for Retail バージョン 10.0.3 の新機能および変更された機能

[!include [banner](../../includes/banner.md)]

このトピックでは、Microsoft Dynamics 365 for Retail 10.0.3 の新機能または変更された機能について説明します。 

Microsoft Dynamics 365 for Finance and Operations の機能については [Finance and Operations バージョン 10.0.3 (2019 年 6 月) の新機能と変更点](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/get-started/whats-new-changed-10-0-3)を参照してください。

## <a name="new-calculation-logic-for-autocharges-in-call-center-for-mixed-delivery-mode-sales-lines"></a>混載配送モードの販売明細行の、コール センターにおける自動請求のための新しい計算ロジック

この機能は既存の自動請求機能を改善し、異なる配送モードが異なるラインに適用されている混合カートに基づいて、小売企業が販売ラインに異なる料金を適用できるシナリオをサポートします。

この機能は、個々の販売ラインの特性に基づいてより現実的な料金の計算を可能にすることで、自動請求の新しい POS 機能に追加機能を追加します。

## <a name="hq-extensions"></a>HQ 拡張機能 

このリリースは Dynamics 365 for Retail のカスタマイズがより簡単となる多数の拡張ポイントを追加します。 カスタム拡張シナリオをサポートするために、次の拡張ポイントが追加されました。

- Retail Headquarters: 拡張性をサポートするためにリファクターされたメソッド。 これらのメソッドはリファクターされ、コマンド チェーン、デリゲート、またはメンバーへのアクセスの提供によって、拡張性をサポートします。
- メソッド:

    - 注文の取得
 
        1. RetailTransactionTransformer.readTransactionSalesTrans
        1. RetailTransactionServiceOrders.createCustomerOrder
        1. Salesline.Insert
        1. Salesline.update

    - 販売促進

        1. RetailBarCodeManagement.CreateBarCodeNoDim
        1. EcoResProductRelationtable.validateWrite

## <a name="additional-resources"></a>追加リソース

### <a name="dynamics-365-april-19-release-notes"></a>Dynamics 365 2019 年 4 月 リリース ノート

当社のビジネス アプリやプラットフォームの次回および最近リリースされた機能について検討中ですか?

[2019 年 4 月リリース ノートをご覧ください](https://docs.microsoft.com/business-applications-release-notes/April19/index)。 あらゆる詳細情報を端から端まで徹底的に捕捉して一元化しました。計画を策定する際に 1 つのドキュメントでそれらの情報を参照できます。
