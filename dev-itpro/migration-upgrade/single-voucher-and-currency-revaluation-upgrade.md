---
title: "工程バージョン1611、Microsoft Dynamics 365の単一伝票、および通貨切り上げのアップグレード"
description: "組織が複数の顧客または仕入先がある、売掛金勘定または買掛金勘定で外貨の再評価プロセス実行して単一伝票を含む仕訳帳を入力します。 このトピックでは、バージョン1611では、Microsoft Dynamics 365にアップグレードすると、これらの場合、組織で実行する手順について説明します。"
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

# <a name="single-voucher-and-currency-revaluation-upgrade-for-microsoft-dynamics-365-for-operations-version-1611"></a>工程バージョン1611、Microsoft Dynamics 365の単一伝票、および通貨切り上げのアップグレード

組織が複数の顧客または仕入先がある、売掛金勘定または買掛金勘定で外貨の再評価プロセス実行して単一伝票を含む仕訳帳を入力します。 このトピックでは、バージョン1611では、Microsoft Dynamics 365にアップグレードすると、これらの場合、組織で実行する手順について説明します。

工程バージョン1611では、Microsoft Dynamics 365にアップグレードすると次の手順に従います。

1.  Dynamics 365 for Operationsにアップグレードする前に、売掛金勘定または買掛金勘定の外貨の再評価プロセスを実行します。 **方法**フィールドを設定します。**請求日**。 最後の外貨の再評価を取り消す再評価のトランザクションが作成されます。 したがって、未処理トランザクションが元の会計通貨で評価されます。
2.  工程バージョン1611 for Operations 365にアップグレードします。
3.  売掛金勘定を実行すると買掛金勘定の外貨の再評価を再度処理します。 この時刻は、**方法**フィールドに設定された**標準**。 現在の為替レートに基づいて新しい再評価のトランザクションが作成されます。 このトランザクションは、未実現利益/損失、正しい集計勘定科目を記録します。



