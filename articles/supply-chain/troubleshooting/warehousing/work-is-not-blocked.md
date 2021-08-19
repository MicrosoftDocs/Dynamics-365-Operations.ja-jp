---
title: 作業はブロックされていない
description: 作業はブロックされていない
author: perlynne
ms.date: 04/15/2021
ms.topic: troubleshooting
ms.search.form: WHSWorkTable_WHSWorkUnblocking
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-05-15
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 6b4361682246397732e8326b98b1b86ff878664e54c8c352296b0d7eaff6bbbd
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/05/2021
ms.locfileid: "6719554"
---
# <a name="work-isnt-blocked"></a>作業はブロックされていない

エラー コード: WHSUnblockNotBlockedWorkErrorMessage

## <a name="symptoms"></a>現象

システムは次のエラー メッセージを表示します。

> ID %1 の作業はブロックされていません。

## <a name="cause"></a>原因

ウェーブの **ブロックされたウェーブ** オプションは、*いいえ* に設定されています。 現在ブロックされていないので、作業のブロックを解除できません。

## <a name="resolution"></a>解像度

 **ブロックされたウェーブ** オプションが *はい* に設定されている場合のみ、ブロックを解除できます。
