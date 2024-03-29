---
title: サービス契約の作成および締結の概要
description: サービス契約では、標準的なサービス訪問で使用されるリソース、およびそれらのリソースに関する顧客への請求方法を定義できます。
author: sorenva
ms.date: 07/25/2019
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: SMAAgreementTable
audience: Application User
ms.reviewer: kamaybac
ms.assetid: ''
ms.search.region: Global
ms.author: sorenand
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: cf28619e66fa5d3e86bdbb3838dc7f711916bcec
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/03/2022
ms.locfileid: "8905605"
---
# <a name="develop-and-establish-service-agreements-overview"></a>サービス契約の作成および締結の概要

[!include [banner](../includes/banner.md)]

サービス契約では、標準的なサービス訪問で使用されるリソース、およびそれらのリソースに関する顧客への請求方法を定義できます。

サービス契約はすべてプロジェクトに関連付けられ、そのプロジェクトを通じてトランザクションの転記と請求が行われます。 ただし、最初にサービス注文をサービス契約と関連付けずに、サービス注文トランザクションをプロジェクトを通して直接請求できます。 サービス注文が 1 回のみのサービス訪問であり、サービス トランザクションをすぐに処理する必要性が、顧客に関する詳細なサービス契約情報を一定期間にわたって管理する必要性を上回る場合、これを行う場合があります。

## <a name="service-agreement"></a>サービス合意

各サービス合意で、プロジェクト、サービス合意 ID、およびサービス合意グループを指定する必要があります。 サービス契約グループを使用して、サービス契約を並べ替えたり、組織したりすることができます。

サービス契約のヘッダーには、関連付けられるすべての契約項目に適用される設定が含まれます。

-  サービス合意を中断するかどうか。 サービス合意が中断されている場合は、サービス合意からサービス注文を生成することができません。
-  サービス合意の期間。
-  サービス注文明細行をサービス注文に連結する方法。
-  サービス合意がテンプレートかどうか。

サービス契約ヘッダーでは、契約のさまざまな行に関連付けられているサービス タスクまたはサービス対象を入力することにより、サービス契約で使用できるサービス対象およびサービス タスクすべてを設定できます。

また、サービス契約ヘッダーから、サービス契約項目またはサービス テンプレート行を現在のサービス契約にコピーすることもできます。

サービス合意を中断し、個々のサービス合意項目を停止できます。

サービス合意で **中断** チェック ボックスをオンにすると、次の操作は実行できません。

-    サービス合意から自動または手動でサービス注文を作成する。

サービス合意で **停止済** チェック ボックスをオンにすると、次の操作は実行できません。

-    サービス合意項目から自動または手動でサービス注文を作成する。
-    サービス合意項目を別のサービス合意またはサービス注文にコピーする。


> [!NOTE]
> サービス契約を中断すると、関連付けられているすべての項目が、それぞれの状態に関係なく停止します。

## <a name="service-agreement-lines"></a>サービス合意項目

各サービス契約項目は、提出されるサービス作業の内容を詳細に説明したものです。 項目には、以下の設定が含まれます。

-  トランザクション タイプ、およびトランザクション タイプの説明。
-  サービス作業を実行する従業員。
-  サービス合意のサービスを実行する必要がある対象。
-  サービス作業が実行されて関連付けられた品目、経費、および手数料の各トランザクションが登録される頻度。
-  サービス注文明細行をサービス注文にグループ化できる時間枠。
-  契約項目のセットをまとめて作業タスクにグループ化するために使用されるサービス タスク。サービス タスクは、サービス技術者や顧客に対する、提供されるサービス タスクの全体的な説明としても使用されます。
-  明細行が停止されるかどうか。 明細行が停止されている場合は、その明細行についてのサービス注文を作成できません。
-  カテゴリや明細行プロパティなどの、プロジェクト設定。

## <a name="related-articles"></a>関連記事

[サービス契約の作成](create-service-agreements.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]