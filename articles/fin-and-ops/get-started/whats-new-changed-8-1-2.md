---
title: "Dynamics 365 for Finance and Operations バージョン 8.1.2 (2018 年 11 月) の新機能および変更された機能"
description: "このトピックでは、Dynamics 365 for Finance and Operations バージョン 8.1.2 の新機能または変更された機能について説明します。 このバージョンは 2018 年 11 月にリリースされました。"
author: tonyafehr
manager: AnnBe
ms.date: 11/13/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Developer, IT Pro
ms.reviewer: tfehr
ms.search.scope: Operations
ms.custom: 
ms.assetid: b364a31d-52de-45c5-b698-64c5262c592a
ms.search.region: Global
ms.author: tfehr
ms.search.validFrom: 2018-11-02
ms.dyn365.ops.version: Release 8.1.2
ms.translationtype: HT
ms.sourcegitcommit: cc995b474e86272b49629f97e1b4d4b4fb597b9d
ms.openlocfilehash: 99703745362f80fcd1d99ddda344772ac659230a
ms.contentlocale: ja-jp
ms.lasthandoff: 12/04/2018

---
# <a name="whats-new-or-changed-in-dynamics-365-for-finance-and-operations-version-812-november-2018"></a>Dynamics 365 for Finance and Operations バージョン 8.1.2 (2018 年 11 月) の新機能および変更された機能

[!include [banner](../includes/banner.md)]
[!include [banner](../includes/preview-banner.md)]

このトピックでは、Microsoft Dynamics 365 for Finance and Operations バージョン 8.1.2 の新機能または変更された機能について説明します。 このバージョンは 2018 年 11 月にリリースされ、ビルド番号は 8.1.195 です。

Microsoft Dynamics 365 for Retail の最新リリースの新機能と変更については、[Dynamics 365 for Retail の新機能と変更点](https://docs.microsoft.com/en-us/dynamics365/unified-operations/retail/get-started/whats-new)を参照してください。

### <a name="dynamics-365-october-18-release-notes"></a>Dynamics 365 2018 年 10 月リリース ノート
当社のビジネス アプリやプラットフォームの次回および最近リリースされた機能について検討中ですか? 

[2018 年 10 月リリース ノートを確認](https://go.microsoft.com/fwlink/?linkid=870424). あらゆる詳細情報を端から端まで徹底的に捕捉して一元化しました。計画を策定する際に 1 つのドキュメントでそれらの情報を参照できます。 

## <a name="bug-fixes"></a>バグ修正
プラットフォーム更新 22 の一部である更新プログラムのそれぞれに含まれるバグ修正については、Lifecycle Services (LCS) にログインし、[KB 資料](https://go.microsoft.com/fwlink/?linkid=2037783) (**未公開**) を参照してください。

## <a name="platform-update-22"></a>プラットフォーム update 22
プラットフォーム更新プログラム 22 を含む Microsoft Dynamics 365 for Finance and Operations バージョン 8.1.2。 プラットフォーム更新プログラム 21 に関する詳細については、[Dynamics 365 for Finance and Operations プラットフォーム更新プログラム 21 (2018 年 11 月) の新機能および変更された機能](whats-new-platform-update-22.md) を参照してください。

## <a name="extensibility-enhancements"></a>拡張性の強化
Finance and Operations の今回のリリースでは、列挙、メタデータ、メソッドの強化など、拡張性をサポートするために、さまざまな拡張機能の強化が加えられています。 詳しくは、[Dynamics 365 for Finance and Operations バージョン 8.1.2 の拡張機能の変更](../../dev-itpro/extensibility/extensibility-changes-812.md)をご覧ください。

## <a name="derived-dimension-values"></a>派生分析コード値
今回のリリースには、派生した分析コード値の変更を防止し、派生した分析コード値で既存の分析コード値を上書きできるようにする機能が含まれています。 詳細については、「[財務分析コード](../../financials/general-ledger/financial-dimensions.md)」を参照してください。


## <a name="third-party-miscellaneous-charges-for-russia"></a>ロシアのサード パーティの雑費
今回のリリースには、次の制度によってサード パーティの雑費と配賦を登録する機能が含まれています。 
- 購入済商品の原価に含める (他の仕入先からの請求書の明細行に配賦) 
- 第三者に再振出 
- その他の経費勘定の再割り当て


## <a name="intrastat-format-changes-for-belgium"></a>ベルギーのイントラスタット形式の変更
今回のリリースには、2019 年の報告に適用されるベルギーの XML イントラスタット形式への変更が含まれています。 新しい形式を適用するには、LCS 共有資産ライブラリから ER コンフィギュレーションの次のバージョン (またはそれ以降のバージョン) をインポートする必要があります: Intrastat (BE).version.2.6.xml。 コンフィギュレーションをインポートする方法の詳細については、[Lifecycle Services からコンフィギュレーションをインポートする](../../dev-itpro/analytics/tasks/er-import-configuration-lifecycle-services.md)を参照してください。 


