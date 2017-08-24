--- 
title: "生産フロー バージョンの有効期限の定義"
description: "特定の日付の生産フロー バージョンの有効性と処理を終了する、または有効なバージョンから新しいバージョンへの変更を計画するために、バージョンの有効期限を設定する必要があります。"
author: cvocph
manager: AnnBe
ms.date: 10/07/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: conradv
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 9b947a02be981155053e33a4ef20e19bf2a194a5
ms.openlocfilehash: b968502de357779b7d26a5780f3febc3076dd9ad
ms.contentlocale: ja-jp
ms.lasthandoff: 07/27/2017

---
# <a name="define-an-expiry-date-for-a-production-flow-version"></a>生産フロー バージョンの有効期限の定義

[!include[task guide banner](../../includes/task-guide-banner.md)]

特定の日付の生産フロー バージョンの有効性と処理を終了する、または有効なバージョンから新しいバージョンへの変更を計画するために、バージョンの有効期限を設定する必要があります。 そのバージョンを無効化する必要はありません。


## <a name="set-an-expiration-date-to-end-a-production-flow-version"></a>生産フロー バージョンを終了する有効期限を設定します。
1. [生産管理] > [設定] > [リーン生産フロー] > [生産フロー] の順に移動します。
2. 一覧で、目的のレコードを見つけ、選択します。
    * 既に定義されているバージョンがある生産フローを選択します。  
3. 一覧で、選択された行のリンクをクリックします。
4. [編集] をクリックします。
5. 一覧で、選択された行をマークします。
6. [有効期限] フィールドに日時を入力します。
    * 有効期限においては、新しいバージョンが開始されたり、または有効化されません。 また、この生産フローのジョブを作成するか、または開始することもできなくなります。 しかし、有効期限以降に開始したジョブは完了できます。  


