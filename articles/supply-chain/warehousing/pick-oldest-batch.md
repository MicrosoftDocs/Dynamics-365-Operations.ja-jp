---
title: モバイル デバイスで最も古いバッチをピッキングする
description: この記事では、オプションを設定および適用し、モバイル デバイスから最も古いバッチをピッキングする方法について説明します。
author: Mirzaab
ms.date: 05/26/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSRFMenuItem
audience: Application User
ms.reviewer: kamaybac
ms.custom: 269384
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: ad1f2cfd029d71784d5efcc169178a791f0ae077
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/03/2022
ms.locfileid: "8885641"
---
# <a name="pick-oldest-batch-on-a-mobile-device"></a>モバイル デバイスで最も古いバッチをピッキング

[!include [banner](../includes/banner.md)]

モバイル デバイス メニューから **最も古いバッチをピッキング** の構成にアクセスすることができるため、これにより、倉庫作業者が現在の場所で一番古いバッチを選択するように強制するまたは警告することができます。  

## <a name="where-it-applies"></a>該当する場合
最も古いバッチをピッキングがモバイル デバイスのメニュー項目で構成され、下記にある項目のバッチのピッキングに影響を与えます。

## <a name="how-to-set-up-the-configuration-for-pick-oldest-batch"></a>最も古いバッチをピッキングの構成を設定する方法 
既存の作業を使用するように設定されている品目については、モバイル デバイス メニューで **最も古いバッチをピッキング** を **なし**、**警告**、または **強制** に設定できます。

**なし**: 作業者にはメッセージは表示されず、現在の場所にあるどのバッチでもピッキングが許可されています。

**警告** および **強制**: 作業者が、バッチを選択すると、有効期限日がもっとも古いバッチの一覧がバッチ コントロールの上に表示されます。 場所がライセンス プレートで制御されている場合、最も古いバッチを持つナンバー プレートのリストがナンバー プレート コントロールの上に表示されます。 
-   **警告**: 表示されている一覧の上にあるライセンス プレートまたはバッチを選択すると、コントロールが非表示になり、古いバッチを選択できるという警告が表示されます。 作業を続行できるようにするには、作業者は同じライセンス プレートまたはバッチを再度選択できます。  
-   **強制**: 作業者には、さらに古いバッチのピッキングがあるというメッセージが引き続き表示されます。


[!INCLUDE[footer-include](../../includes/footer-banner.md)]