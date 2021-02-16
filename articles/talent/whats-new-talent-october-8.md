---
title: Dynamics 365 Talent - Core HR (2018 年 10 月 8 日) の新機能および変更された機能
description: このトピックでは、Microsoft Dynamics 365 Talent - Core HR の新機能または変更された機能について説明します。
author: Darinkramer
manager: AnnBe
ms.date: 10/07/2018
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
ms.search.validFrom: 2018-10-07
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 30c148a1bf27a221c1d4feacbe89cabfc412872c
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/13/2020
ms.locfileid: "4461763"
---
# <a name="whats-new-or-changed-in-dynamics-365-talent---core-hr-october-8-2018"></a>Dynamics 365 Talent - Core HR (2018 年 10 月 8 日) の新機能および変更された機能

**ビルド 8.1.1050.0**

このトピックでは、Core HR の新機能または変更された機能について説明します。

## <a name="allow-other-dates-to-be-used-on-leave-tier-basis-leave-management"></a>休暇層基準 (休暇管理) で他の日付を使用する許可

従業員への報奨休暇の場合、報奨層基準によって従業員が見越計上する休暇時間が決定されます。 現在、これらの層は従業員の開始日および勤続日数に基づいています。 一部のシナリオにおいて、組織には、これらの層が記念日または元の採用日付などの、他の日付に基づいているようにする必要があります。 これらの日付は、見越計上が発生する時を決定するために休暇計画で既に使用されており、これら同じ日付が従業員が計画に登録される時に使用される機能は、見越計上金額を決定するために追加されています。 

## <a name="other-changes"></a>その他の変更
その他の修正プログラムは今回のリリースに含まれています。

## <a name="known-issue"></a>既知の問題

**問題:** 作業者に新しい添付ファイルを追加する場合、**新規** および **編集** ボタンは灰色表示です。**回避策:** 添付ファイル ページを開く前に、**作業者** ページの Factbox が閉じていることを確認します。 **作業者** ページが読み込まれる時、FactBoxes が閉じている場合には、添付ファイルボタンが有効になります。 (この問題は次のプラットフォーム更新プログラムで修正されます。)
