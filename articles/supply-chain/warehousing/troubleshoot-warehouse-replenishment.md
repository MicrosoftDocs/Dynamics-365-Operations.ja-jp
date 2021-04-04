---
title: 倉庫の補充のトラブルシューティング
description: このトピックでは、Microsoft Dynamics 365 Supply Chain Management での倉庫補充の処理中に発生する可能性がある問題を修正する方法について説明します。
author: perlynne
manager: tfehr
ms.date: 10/19/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2020-10-19
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 8dfb58c9156df106f58dfdc0ee2e0ef8defb9d9f
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/15/2021
ms.locfileid: "5263207"
---
# <a name="troubleshoot-warehouse-replenishment"></a>倉庫の補充のトラブルシューティング

[!include [banner](../includes/banner.md)]

このトピックでは、Microsoft Dynamics 365 Supply Chain Management での倉庫補充の処理中に発生する可能性がある問題を修正する方法について説明します。

## <a name="i-receive-the-following-error-message-work-1-cannot-be-unblocked-because-it-has-unfinished-replenishment-work"></a>エラー メッセージ "完了していない補充作業があるために作業 %1 をブロック解除できません" が表示されます。

### <a name="issue-description"></a>問題の説明

ピッキング作業は、依存する補充作業のためブロックされます。

### <a name="issue-resolution"></a>問題の解決

ウェーブ需要補充を使用するとき、ソース注文需要を満たすためにピッキング場所を補充する必要がある場合、補充作業とピッキング作業の両方がシステムによって作成されます。 ただし、補充作業が完了するまで、ピッキング作業はブロックされます。 補充作業が完了していない場合は、ピッキング場所に十分な在庫がないので、この動作は意図的です。 補充作業を完了し、ピッキング作業を処理します。


[!INCLUDE[footer-include](../../includes/footer-banner.md)]