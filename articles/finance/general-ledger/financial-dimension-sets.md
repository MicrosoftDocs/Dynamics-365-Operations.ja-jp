---
title: 財務分析コード セット
description: この記事では、財務分析コード セットについて説明し、その使用を最適化するためのヒントを提供します。
author: yukonpeegs
ms.date: 03/07/2022
ms.topic: article
ems.prod: ''
ms.technology: ''
ms.search.form: DimensionFocus, LedgerTrialBalanceListPage
audience: Application User
ms.reviewer: twheeloc
ms.custom: 25871
ms.search.region: Global
ms.author: epegors
ms.search.validFrom: 2021-03-23
ms.dyn365.ops.version: 10.0.16
ms.openlocfilehash: 3d4c15504b2ad128493e1bafa36aed271c2ab6dc
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/03/2022
ms.locfileid: "8864284"
---
# <a name="financial-dimension-sets"></a>財務分析コード セット

[!include [banner](../includes/banner.md)]

この記事では、財務分析コード セットについて説明し、その使用を最適化するためのヒントを提供します。

分析コード セットは、一般会計データをユーザー定義の方法で集計するために使用できる財務分析コードの順序付きリストです。 分析コード セットの主な用途は、試算表を定義することです。

標準分析コード セットだけが、主勘定のみを含む分析コード セットになります。

**財務分析コード セット** ページを使用して、財務分析コード セットの作成と管理を行うことができます。

## <a name="dimension-set-balances"></a>分析コード セットの残高

分析コード セットには、財務分析コードに基づく残高があります。 残高は、分析コード セットの定義に基づいて一般会計に存在します。 残高は一般会計データから集計され、取得時のパフォーマンスを向上させることができます (試算表の生成時など)。

## <a name="create-balances"></a>残高の作成

**残高の作成** ボタンを使用して、現在残高が存在しない分析コード セットの残高を初期化します。

> [!NOTE]
> 残高の更新はすべての一般会計の転記活動に影響を与えるので、残高がある分析コード セットの数を制限することをお勧めします。

## <a name="update-balances"></a>残高の更新

**残高の更新** ボタンを使用して、最新の一般会計の転記活動を残高に含めます。 残高の更新は、軽い操作です。 最後の更新以降に発生した一般会計の転記活動のみを処理する必要があります。

> [!NOTE]
> 試算表の表示によって強制的に更新し、確実に現在の残高を表示します。 定期バッチ ジョブの使用を検討すると、最も頻繁に使用する分析コード セットの更新を高速に行えます。 このようにして、試算表のユーザーの待ち時間を最小限にすることができます。

## <a name="rebuild-balances"></a>残高の再構築

**残高の再構築** ボタンを使用して、最初から残高を再作成します。 このようにして、確実に一般会計のデータと一致させることができます。 残高の再構築には多くの処理が必要であり、通常は必要ではありません。

> [!NOTE]
> 定期的に残高の再構築が必要なシナリオがある場合は、カスタマー サポートに問い合わせることをお勧めします。 カスタマー サポートは、残高が一般会計のデータと一致しない理由を特定するのに役立ちます。

## <a name="clear-balances"></a>残高のクリア

**残高のクリア** ボタンを使用して残高を削除し、それ以上の更新を停止します。 分析コード セットによる一般会計の転記活動への影響はなくなりました。

## <a name="delete-a-dimension-set"></a>分析コードセットの削除

特定の分析コード **セットの残高データに** 関する潜在的な問題を解決するために、分析コード セットを任意の形式で削除および再作成しません。 分析コード セットを再作成すると、原価が計算されます。 問題に関する詳細については、カスタマ サポートに問い合わせてください。 


詳細については、「[財務分析コード](financial-dimensions.md)」を参照してください。

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
