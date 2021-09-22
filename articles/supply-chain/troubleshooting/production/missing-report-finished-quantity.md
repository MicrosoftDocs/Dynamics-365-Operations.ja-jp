---
title: 数量の欠落エラーにより完了レポートの更新が失敗する
description: エラーの数量を報告しているが、時間または材料の数量を報告していないときに、製造オーダーを終了しようとすると、完了レポートの更新は失敗します。
author: SmithaNataraj
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: smnatara
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 7785549c47063727f2749749940c1a96a351e70f
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/07/2021
ms.locfileid: "7476847"
---
# <a name="report-as-finished-update-fails-with-a-missing-quantity-error"></a>数量の欠落エラーにより完了レポートの更新が失敗する

## <a name="symptoms"></a>現象

エラーの数量を報告しているが、時間または材料の数量を報告していないときに、製造オーダーを完了として報告することを試みます。 製造オーダーを終了しようとすると、完了レポートの更新が失敗し、次のエラー メッセージが表示されます。

> 完了レポートの数量がありません。

## <a name="resolution"></a>解決策

製造オーダーのエラー数量を報告する場合、正常数量も報告する必要があります。
