---
title: 生産フロー バージョンの有効期限の定義
description: 特定の日付の生産フロー バージョンの有効性と処理を終了する、または有効なバージョンから新しいバージョンへの変更を計画するために、バージョンの有効期限を設定する必要があります。
author: cvocph
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LeanProductionFlow
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: a595ca4ff9f6753631303b656d56735320a22a69
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/15/2021
ms.locfileid: "4975088"
---
# <a name="define-an-expiry-date-for-a-production-flow-version"></a>生産フロー バージョンの有効期限の定義

[!include [banner](../../includes/banner.md)]

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



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]