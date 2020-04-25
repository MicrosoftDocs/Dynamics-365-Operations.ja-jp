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
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: conradv
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 3d942f54b2739f2ca3dcc3e8b8a497166a8edb42
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/02/2020
ms.locfileid: "3212092"
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

