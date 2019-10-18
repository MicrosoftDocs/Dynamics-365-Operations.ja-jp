---
title: Microsoft Dynamics 365 Talent - Attract における Broadbean 統合の有効化
description: このトピックでは、Broadbean などの外部の職務ボードへジョブを転記するための Microsoft Dynamics 365 Talent - Attract のコンフィギュレーション方法について説明します。
author: andreabichsel
manager: AnnBe
ms.date: 07/08/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent, Core
ms.custom: 7521
ms.assetid: 3b953d5f-6325-4c9e-8b9b-6ab0458a73f8
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2019-07-08
ms.dyn365.ops.version: Talent October 2018 update
ms.openlocfilehash: 808f91fb4b68ba9b5cee54d86423d23232df23a4
ms.sourcegitcommit: 434dd21450bddcd891aba0555b9853d9ba0afb6f
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/23/2019
ms.locfileid: "2008596"
---
# <a name="enable-broadbean-integration"></a>Broadbean との統合を有効にする

[!include[banner](../includes/banner.md)]

できるだけ多くの資格のある候補者の前で、空いている職位を獲得する必要があります。 Broadbean などの採用サイトは、この目標を達成するのに役立ちます。 Microsoft Dynamics 365 Talent: Attract では Broadbean にジョブを転記し、Microsoft がこの領域で新製品を常に提供できるようにします。

> [!NOTE]
> - 外部サイトへジョブを転記するには、[包括採用アドオン](https://docs.microsoft.com/dynamics365/unified-operations/talent/attract-comprehensive-hiring) が必要です。
> - Attract から Broadbean にジョブを転記するには、Broadbean サブスクリプションが必要です。
> - 現在プレビューにある機能です。 試行する場合は、[Attract 管理者の設定で有効にする](https://docs.microsoft.com/dynamics365/unified-operations/talent/access-preview-feature) を実行します。

## <a name="configure-broadbean-integration"></a>Broadbean との統合をコンフィギュレーションする

1. Attract に管理者としてサインインします。

2. ページの右上隅にある**設定**ボタン (ギヤ記号) を選択して、**管理者センター**を選択します。

3. Broadbean に連絡して、**ユーザー名**、**クライアント ID**、および**暗号化トークン**フィールドに情報を入力します。

4. **保存** を選択します。

> [!WARNING]
> Broadbean の資格情報は機密性が高いものです。 したがって、責任を持ってそれらを格納および共有します。 Attract の管理者ロールを持つすべてのユーザーは、これらの資格情報を表示できます。

> [!NOTE]
> Microsoft と Attract は、これらの値を作成し管理することには関与していません。 Attract でそれらを最新の状態に保ち、Broadbean と協力してユーザーの資格情報に関連する問題を解決するのはユーザー個人の責任となりす。
