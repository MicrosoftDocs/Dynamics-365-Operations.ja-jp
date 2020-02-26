---
title: 小売店舗の明細書の作成、計算、および転記
description: このトピックでは、店舗の明細書を作成、計算、および転記する手動のステップについて説明します。
author: jashanno
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: RetailChannelOperationsWorkspace, RetailStatementTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: jashanno
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 3b26ea5c816339eef88bfdd9ac59701dcaa31fe4
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/01/2020
ms.locfileid: "3023170"
---
# <a name="create-calculate-and-post-statements-for-a-retail-store"></a>小売店舗の明細書の作成、計算、および転記

[!include[task guide banner](../includes/task-guide-banner.md)]

このトピックでは、店舗の明細書を作成、計算、および転記する手動のステップについて説明します。 同じタスクにコンフィギュレーションできるバッチ ジョブもあります。 他のトピックで、バッチ ジョブをコンフィギュレーションし、実行するための手順を検索できます。 この手順を完了するには、POS で完了して Dynamics 365 Commerce で取り出されたトランザクションが必要です。 この記録では、デモ データの会社 USRT を使用します。

1. ホーム ページから**店舗の財務**を選択します。
2. **新しい明細書**を選択します。
3. **店舗番号**フィールドで、ドロップダウンからオプションを選択します。
4. **OK** を選択します。
5. **設定**グループには、どのトランザクションを明細書に含めるか、どのように明細行にグループ化するかを制御する設定があります。 **設定**グループを開き、これらの設定を変更することもできますが、既定値を使用することもできます。  
    - **明細書の方法**フィールドで明細行をグループ化する方法を定義します。  
    - 特定のスタッフ メンバーまたはレジスターの明細書のみ計算する場合、スタッフ メンバーまたはレジスターを**スタッフ/レジスター** フィールドで選択します。  
6. **決済方法**フィールドで、オプションを選択します。
7. アクション ウィンドウから**明細書の計算**を選択します。
8. **はい**を選択します。
    - 明細書を計算した後、各支払方法の合計金額と使用された明細書の方法が記された行が作成されます。  
    - 入力、または更新する必要がある場合、各行に計算済金額を入力します。 計算済フィールドには、POS で実行した支払/入金申告の金額が表示されます。  
9. アクション ウィンドウから**明細書の転記**を選択します。
10. **閉じる**を選択します。
11. ウィンドウを閉じます。
12. ホーム ページで、**店舗の財務**を選択します。
13. **転記済明細書**タブを選択します。

