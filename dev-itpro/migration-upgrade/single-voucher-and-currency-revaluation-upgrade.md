---
title: "単一伝票と通貨再評価のアップグレード"
description: "一部の組織では、複数の顧客または仕入先がある単一伝票を含む仕訳帳を入力し、売掛金勘定または買掛金勘定の外貨再評価プロセスも実行します。 このトピックでは、これらの組織が Microsoft Dynamics 365 for Operations バージョン 1611 にアップグレードする際に従うべき手順について説明します。"
author: twheeloc
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Application User
ms.search.scope: Operations, Core
ms.custom: 265364
ms.assetid: c61391e4-c4bf-4f09-bd18-8107a1bf055e
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: d3c6d817424be79b09ccdd89deb7f31599fe9bf5
ms.contentlocale: ja-jp
ms.lasthandoff: 05/25/2017


---

# <a name="single-voucher-and-currency-revaluation-upgrade"></a>単一伝票と通貨再評価のアップグレード

[!include[banner](../includes/banner.md)]


一部の組織では、複数の顧客または仕入先がある単一伝票を含む仕訳帳を入力し、売掛金勘定または買掛金勘定の外貨再評価プロセスも実行します。 このトピックでは、これらの組織が Microsoft Dynamics 365 for Operations バージョン 1611 にアップグレードする際に従うべき手順について説明します。

Microsoft Dynamics 365 for Operations バージョン 1611 にアップグレードする際には次の手順に従います。

1.  Dynamics 365 for Operations にアップグレードする前に、売掛金勘定または買掛金勘定用の外貨再評価プロセスを実行します。 [**メソッド**] フィールドを **請求日** に設定します。 最後の外貨再評価を取り消す再評価トランザクションが作成されます。 したがって、未処理トランザクションは元の会計通貨で評価されます。
2.  Dynamics 365 for Operations バージョン 1611 にアップグレードします。
3.  売掛金勘定および買掛金勘定の外貨再評価プロセスを再実行します。 今回は、[**メソッド**] フィールドを **標準** に設定します。 現在の為替レートに基づいた新しい再評価トランザクションが作成されます。 このトランザクションは、含み益 / 損失と正しい集計勘定科目を記録します。





