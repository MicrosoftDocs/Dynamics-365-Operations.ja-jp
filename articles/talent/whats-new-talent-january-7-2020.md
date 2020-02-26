---
title: Dynamics 365 Talent (2020 年 1 月 7 日) の新機能および変更された機能
description: この記事では、Microsoft Dynamics 365 Talent の新機能または変更された機能について説明します。
author: Darinkramer
manager: AnnBe
ms.date: 01/07/2020
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
ms.search.validFrom: 2020-01-07
ms.dyn365.ops.version: Talent
ms.openlocfilehash: e227c614fdbfe6f3dd410f1a533c593979abf1ec
ms.sourcegitcommit: 615ed3e4260192ba36826e128f1afa1588e94845
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/21/2020
ms.locfileid: "2974433"
---
# <a name="whats-new-or-changed-in-dynamics-365-talent-january-7-2020"></a>Dynamics 365 Talent (2020 年 1 月 7 日) の新機能および変更された機能

この記事では、Dynamics 365 Talent の新機能および変更された機能について説明します。

## <a name="changes-in-attract"></a>Attract の変更

今回のリリースには、Dynamics 365 Talent: Attract のマイナーなバグ修正が含まれています。

## <a name="changes-in-onboard"></a>Onboard の変更

今回のリリースには、Dynamics 365 Talent: Onboard のマイナーなバグ修正が含まれています。

## <a name="changes-in-core-hr"></a>Core HR の変更

このセクションに記載された変更は、ビルド番号 8.1.2697 に適用されます。 ヘッダーにあるかっこ内の数字は、Microsoft Dynamics Lifecycle Services (LCS) のサポート番号を参照していることがあります。

 
### <a name="cant-delete-workers-that-dont-have-employment-records---386157"></a>雇用レコードがない作業者を削除できない - (386157)

この変更により、**雇用なし作業者**フォームに削除オプションが追加されます。 作業者の将来雇用、現職、または過去の職歴が存在しない場合は、作業者がこのフォームで表示されます。 このリリースでは、システム管理者に対してのみ削除が有効になります。 ただし、来週のリリースでは、HR アシスタント ロールのすべてのユーザーが雇用なし従業員を削除できるよう、セキュリティが更新されます。 これらの変更は、次の手順に従って手動で行うこともできます。

1. **セキュリティのコンフィギュレーション**に移動します。
2. **権限**タブで、**権限**リストを**作業者の管理**にフィルター処理します。
3. **参照**列で、**メニュー項目の表示**を選択します。
4. **メニュー項目の表示**列で、**HcmWOrkersWithoutEmployment** を選択します。
5. **削除**のアクセス許可を付与するよう設定します。
6. **未公開のオブジェクト** タブを選択します。
7. **すべて公開**を選択します。
