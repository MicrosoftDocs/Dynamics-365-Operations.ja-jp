---
title: ウィザードを使用した番号順序の設定
description: このトピックでは、ウィザードを使用して必要なすべての番号順序を同時に設定する方法を説明します。
author: SunilGarg
ms.date: 07/18/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: NumberSequenceTableListPage, NumberSequenceWizard
audience: Application User
ms.reviewer: sericks
ms.search.region: Global
ms.author: sunilg
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 7388a835147e1e8242463fee98c57c300d062877
ms.sourcegitcommit: 8cb031501a2b2505443599aabffcfece50e01263
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/09/2021
ms.locfileid: "7777571"
---
# <a name="set-up-number-sequences-using-a-wizard"></a>ウィザードを使用した番号順序の設定

[!include [banner](../../includes/banner.md)]

番号順序は、マスタ データ レコードおよびトランザクション レコードに必要な読みやすい固有 ID の生成に使用されます。 ID が必要なマスタ データまたはトランザクション レコードは、参照先と呼ばれます。 参照先に新しいレコードを作成するには、事前に番号順序を設定して参照先に関連付ける必要があります。 このトピックでは、ウィザードを使用して必要なすべての番号順序を同時に設定する方法を説明します。 この手順の作成に使用するデモ データの会社は USMF です。

1. **ナビゲーション > モジュール > 組織管理 > 番号順序 > 番号順序** の順に移動します。
2. **生成** を選択します。
3. **次へ** を選択します。

   - このページでは、ID コード、最小値、および最大値を変更できます。 また、番号順序を連続させるかどうかも指定できます。   
   - 番号順序に対して番号を事前に割り当てる必要がある場合は、**連続** オプションは選択しないでください。 番号順序の形式にスコープ区分を追加するには、リストから形式を選択し、**スコープを書式に含める** を選択します。 番号順序の形式からスコープ区分を削除するには、リストから形式を選択し、**書式からスコープを削除** を選択します。 自動生成から番号順序を除外するには、リストから番号順序を選択し、**削除** を選択します。  

4. **次へ** を選択します。
5. **完了** を選択します。



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
