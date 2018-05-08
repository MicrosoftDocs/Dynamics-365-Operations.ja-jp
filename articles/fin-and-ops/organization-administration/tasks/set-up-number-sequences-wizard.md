--- 
title: "ウィザードを使用した番号順序の設定"
description: "番号順序は、マスタ データ レコードおよびトランザクション レコードに必要な読みやすい固有 ID の生成に使用されます。"
author: sericks007
manager: AnnBe
ms.date: 11/10/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: sericks
ms.search.scope: Operations
ms.search.region: Global
ms.author: sericks
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 96c1bc711350b447611977c3f2070fbc08fbae0f
ms.contentlocale: ja-jp
ms.lasthandoff: 09/29/2017

---
# <a name="set-up-number-sequences-by-using-a-wizard"></a>ウィザードを使用した番号順序の設定

[!include [task guide banner](../../includes/task-guide-banner.md)]

番号順序は、マスタ データ レコードおよびトランザクション レコードに必要な読みやすい固有 ID の生成に使用されます。 ID が必要なマスタ データまたはトランザクション レコードは、参照先と呼ばれます。 参照先に新しいレコードを作成するには、事前に番号順序を設定して参照先に関連付ける必要があります。 この手順では、ウィザードを使用して必要なすべての番号順序を同時に設定する方法を説明します。 この手順の作成に使用するデモ データの会社は USMF です。

1. [組織管理] > [番号順序] > [番号順序] の順に移動します。
2. [生成] をクリックします。
3. [次へ] をクリックします。
    * このページでは、ID コード、最小値、および最大値を変更できます。 また、番号順序を連続させるかどうかも指定できます。   
    * 番号順序に対して番号を事前に割り当てる必要がある場合は、[連続] オプションは選択しないでください。     番号順序の形式にスコープ区分を追加するには、リストから形式を選択し、[スコープを書式に含める] をクリックします。     番号順序の形式からスコープ区分を削除するには、リストから形式を選択し、[書式からスコープを削除] をクリックします。     自動生成から番号順序を除外するには、リストから番号順序を選択し、[削除] をクリックします。  
4. [次へ] をクリックします。
5. [完了] をクリックします。


