---
title: 移動オーダー用の倉庫の設定
description: このトピックでは、移動オーダーの倉庫を設定する方法について説明します。
author: Mirzaab
manager: AnnBe
ms.date: 01/18/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2018-4-30
ms.dyn365.ops.version: 8
ms.openlocfilehash: 91db6e8f921bd674211f6d478b6d0f0a832c983c
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/01/2019
ms.locfileid: "1847018"
---
# <a name="set-up-warehouses-for-transfer-orders"></a>移動オーダー用の倉庫の設定 

[!include [banner](../includes/banner.md)]

倉庫レベルを使用して倉庫間の移動オーダーをサポートする階層を作成できます。 この設定に基づいて、マスタ スケジューリングは個々の倉庫レベルにおける在庫品目要求を計算し、割り当てられたソース倉庫から計画移動オーダーを生成してそれらの要求を満たします。

1.  **在庫管理 > 設定 > 在庫詳細 > 倉庫** の順にクリックします。

2.  補充する倉庫を選択します。

3.  **マスター プラン** クイック タブで、**補充**チェック ボックスを選択します。

4.  **主要倉庫**フィールドで、補充倉庫として割り当てる倉庫を選択します。 マスタ スケジューリングは選択した倉庫の移動要求を計算し、割り当てられた**主要倉庫**から計画移動オーダーを生成します。
   
    > [!NOTE]
    > <P><STRONG>補充</STRONG>チェックボックスをオフにすると、<STRONG>主要倉庫</STRONG>に関連する倉庫レベルが選択した倉庫に割り当てられますが、<STRONG>主要倉庫</STRONG>は補充倉庫として設定されません。</P>

5.  ページを閉じて、新しい設定を適用します。


> [!TIP]
> <P>補充用の倉庫を割り当てる場合は、倉庫を<STRONG>保管分析コード グループ</STRONG>ページの保管分析コードとして設定する必要があります。 このページで、倉庫に対する<STRONG>有効</STRONG>フィールドおよび<STRONG>分析コード別補充計画</STRONG>フィールドを選択します。</P>

## <a name="set-up-transport-lead-time"></a>配送のリード タイムの設定

**配送日数**ページの倉庫間で配送のリード タイムを設定することも必要です。 
1. **在庫管理 > 設定 > 配分 > 配送日数**に移動します。
2. **入荷場所**フィールドで、**倉庫**を選択します。
3. **出荷倉庫**、**入荷倉庫**、および**配送日数**を選択します。 
4. (オプション) 荷渡方法によっては、**荷渡方法ごとの配送日数**タブで配送時間を設定することもできます。
