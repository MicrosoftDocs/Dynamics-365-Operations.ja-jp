---
title: 経費ポリシーを定義します
description: Microsoft Dynamics 365 for Finance and Operations では、作業者が経費精算書と出張費要求を入力して提出する際に従う必要がある経費ポリシーを定義できます。
author: ryansandness
manager: AnnBe
ms.date: 04/26/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysPolicyListPage, TrvPolicyRule
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: ryansand
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 26336710b277ce9594c8546f2214e152a3460204
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/01/2019
ms.locfileid: "1840892"
---
# <a name="expense-policies"></a>経費ポリシー

[!include [banner](../includes/banner.md)]

作業者が経費精算書と出張費要求を入力して提出する際に従う必要があるポリシーを定義できます。         
経費ポリシーを実装すると、経費を効率的に管理できます。         

たとえば、ニューヨークでのホテルの 1 泊料金は USD 250 以下にするというホテル経費のポリシーを設定できます。       
経費精算書または宿泊料金がこの金額を超える出張費要求を作業者が提出すると、システムが通知をします        
作業者が、経費に関するポリシー金額を超えました。 作業者が受け取るメッセージをコンフィギュレーションできます        
ポリシーを定義します。      
        
次の 3 種類のポリシーを定義できます。         
        
- 警告: 作業者は経費精算書や出張費要求を提出できますが、経費はすべての承認者にマークされ        
  その後の報告用に。        

- エラー: 経費精算書や出張費要求を提出する前に、経費を変更してポリシーに準拠するように作業者に要求します。       
 
 - 妥当性: 経費精算書や出張費要求を提出する前に、ポリシー金額を超えることに関する妥当性を入力するように作業者または管理者に要求します。        

## <a name="policy-tips"></a>ポリシーのヒント
経費管理に関する新しいポリシーを作成するのに役立つ提案を示します。 
* ポリシーは日付に対して有効であり、経費が発生した日付より後の日付でポリシーが作成されている場合は有効になりません。 たとえば、今日、50 ドルの最大食費を適用する新しいポリシーを作成していて、既存の経費が機能の昨日の日付で入力されている場合、このポリシーはチェックされません。
* 明細化できる経費カテゴリに対するポリシーを作成する場合、経費明細行のタイプの条件を追加することを考慮してください。 レシートを必要とするポリシーは明細行に対しては意味を持たない場合があり、ヘッダー行または非明細行にのみ適用する必要があります。 

## <a name="when-to-evaluate-policies"></a>ポリシーを評価する場合

経費管理パラメータには、明細行を保存する時または経費精算書を送信する時のいずれかの時に経費管理ポリシーを評価するというオプションがあります。 明細行を保存する時に評価するよう選択した場合、ユーザーは経費精算書を一度に完了するために必要な事柄を早く確認できることになります。 それ以外の場合は、ワークフローへの送信中、その終了時に検証が実行されるようにした場合に、ポリシーの評価を遅らせることができ、時間を節約できます。
