---
title: 固定資産の移動
description: このタスク ガイドは、財務分析コード セットのいずれかから新しい財務分析コード セットに、固定資産帳簿の財務情報を転送します。
author: saraschi2
ms.date: 07/22/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: AssetTable, AssetTransfer, DimensionLookup, AssetTransferConfirmation
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 7588e0058713d7facf053aa269210fc88e5a3ff2
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/01/2021
ms.locfileid: "5823887"
---
# <a name="transfer-a-fixed-asset"></a>固定資産の移動

[!include [banner](../../includes/banner.md)]

このタスク ガイドは、財務分析コード セットのいずれかから新しい財務分析コード セットに、固定資産帳簿の財務情報を転送します。  これは USMF の法人に対して経理担当ロールとデモ データを使用します。

1. ナビゲーション ウィンドウで、**モジュール > 固定資産 > 固定資産 > 固定資産** に移動します。
2. 一覧で、固定資産の移動先の場所を選択します。
3. アクション ウィンドウで、**固定資産** をクリックします。
4. **固定資産の移動** をクリックします。
5. **移動日** フィールドに日付を入力します。
6. 転送についてのコメントを入力します。
    
    この一覧には、固定資産のすべての帳簿が表示されます。  
7. 新しい財務分析コード セットに転送する帳簿をマークします。
    * この一覧には、選択した帳簿の既存の財務分析コード値が表示されます。  
    * 選択した固定資産帳簿の更新に必要な財務分析コードを選択します。  
8. **財務分析コード** フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。
    * 必要に応じて他の財務分析コード値を設定します。  
    * 転送が行われると、値が入力されているか、または空白のままであるかに関わらず、すべての財務分析コード値が変更されます。 たとえば、「BusinessUnit」の値を入力し、「CostCenter」と「財務分析コード部門」を空白のままにした場合。 勘定構造により CostCenter と部門に空白の値を入力できる場合は、転送によって各価値モデルの CostCenter に新しい値が挿入され、BusinessUnit および部門は空白となります。  
9. **更新** をクリックします。
    * 転送を終了する前に変更をプレビューする機会があります。  
    * 固定資産の帳簿を転送する前に結果を確認します。  
10. **転送** をクリックします。



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]