---
title: "Microsoft Dynamics 365 for Operations バージョン 1611 の単一伝票と通貨再評価のアップグレード"
description: "一部の組織では、複数の顧客または仕入先がある単一伝票を含む仕訳帳を入力し、売掛金勘定または買掛金勘定の外貨再評価プロセスも実行します。 このトピックでは、これらの組織が Microsoft Dynamics 365 for Operations バージョン 1611 にアップグレードする際に従うべき手順について説明します。"
author: twheeloc
manager: AnnBe
ms.date: 2016-12-28 16 - 04 - 17
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: Operations, Core
ms.custom: 265364
ms.assetid: c61391e4-c4bf-4f09-bd18-8107a1bf055e
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
translationtype: Human Translation
ms.sourcegitcommit: 0c6a7bdc4ba82dd57ab3e395e6dfb0ae4de31fc4
ms.openlocfilehash: d42c753d0dc8b8efc2a0d2a26da32a4951d85503
ms.lasthandoff: 03/31/2017


---

# <a name="single-voucher-and-currency-revaluation-upgrade-for-microsoft-dynamics-365-for-operations-version-1611"></a>Microsoft Dynamics 365 for Operations バージョン 1611 の単一伝票と通貨再評価のアップグレード

一部の組織では、複数の顧客または仕入先がある単一伝票を含む仕訳帳を入力し、売掛金勘定または買掛金勘定の外貨再評価プロセスも実行します。 このトピックでは、これらの組織が Microsoft Dynamics 365 for Operations バージョン 1611 にアップグレードする際に従うべき手順について説明します。

Microsoft Dynamics 365 for Operations バージョン 1611 にアップグレードする際には次の手順に従います。

1.  Dynamics 365 for Operations にアップグレードする前に、売掛金勘定または買掛金勘定用の外貨再評価プロセスを実行します。 [**メソッド**] フィールドを **請求日** に設定します。 最後の外貨再評価を取り消す再評価トランザクションが作成されます。 したがって、未処理トランザクションは元の会計通貨で評価されます。
2.  Dynamics 365 for Operations バージョン 1611 にアップグレードします。
3.  売掛金勘定および買掛金勘定の外貨再評価プロセスを再実行します。 今回は、[**メソッド**] フィールドを **標準** に設定します。 現在の為替レートに基づいた新しい再評価トランザクションが作成されます。 このトランザクションは、含み益 / 損失と正しい集計勘定科目を記録します。



