---
title: Dynamics 365 Talent (2020 年 1 月 14 日) の新機能および変更された機能
description: この記事では、Microsoft Dynamics 365 Talent の新機能または変更された機能について説明します。
author: Darinkramer
manager: AnnBe
ms.date: 01/14/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2020-01-14
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 865ddbc6749d3ea29a258f4c772044307c41bf35
ms.sourcegitcommit: e89bb3e5420a6ece84f4e80c11e360b4a042f59d
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/17/2020
ms.locfileid: "4529117"
---
# <a name="whats-new-or-changed-in-dynamics-365-talent-january-14-2020"></a>Dynamics 365 Talent (2020 年 1 月 14 日) の新機能および変更された機能

[!include [banner](includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

この記事では、Dynamics 365 Talent の新機能および変更された機能について説明します。

## <a name="changes-in-attract"></a>Attract の変更

今回のリリースには、Dynamics 365 Talent: Attract のマイナーなバグ修正が含まれています。

## <a name="changes-in-onboard"></a>Onboard の変更

今回のリリースには、Dynamics 365 Talent: Onboard のマイナーなバグ修正が含まれています。

## <a name="changes-in-core-hr"></a>Core HR の変更

このセクションに記載された変更は、ビルド番号 8.1.2709 に適用されます。 ヘッダーにあるかっこ内の数字は、Microsoft Dynamics Lifecycle Services (LCS) のサポート番号を参照していることがあります。

### <a name="system-unable-to-generate-calendar-days-when-importing-through-data-management-framework-381195"></a>データ管理フレームワーク経由のインポート時に、システムでカレンダー日を生成できない (381195)

この変更により、カレンダー日をインポートするとエラー **無効な日付形式** が生成される問題が修正されます。 このエラーが発生すると、作業カレンダー日単位明細行は作成されません。

## <a name="coming-soon"></a>間もなく公開

次の変更により、新しい Common Data Service ソリューションがまもなく利用可能になります。

| 説明 | 計上額 |
| --- | --- |
| **職務/職位** エンティティの変更 | <ul><li>追加された **報酬地域**</li><li>追加された **財務分析コード**</li></ul> |
| **作業者** エンティティの変更 | <ul><li>追加された **名前の順序**</li><li>追加された **自宅から作業**</li><li>追加された **言語**</li><li>追加された **勤続日数**</li><li>追加された **記念日**</li><li>追加された **元の採用日付**</li></ul> |
| **雇用** エンティティの変更 | <ul><li>追加された **財務分析コード**</li><li>追加された **退職理由**</li><li>**移行日** から名前変更された **退職日**</li><li>追加された **猶予期間**</li></ul> |
| **作業者住所** エンティティの変更 | <ul><li>追加された **番地**</li><li>廃止としてマークされた **住所行 1**、**住所行 2**、および **住所行 3**</li></ul> |
| 新しい変動報酬の設定エンティティ | <ul><li>**変動報酬プラン タイプ**</li><li>**変動報酬プラン**</li><li>**給付ルール**</li><li>**変動報酬プラン レベル**</li></ul> |
| 新しい **作業者カレンダー雇用** エンティティ | <ul><li>追加された **作業カレンダー エンティティ**</li></ul> |


[!INCLUDE[footer-include](../includes/footer-banner.md)]