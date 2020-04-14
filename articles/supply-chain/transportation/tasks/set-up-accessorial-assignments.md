---
title: 付帯サービス割り当ての設定
description: この手順では、付帯サービスの割り当てを設定する方法を示します。
author: ShylaThompson
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: cd951a65d9cfd20952865db81ac58c698aa124a7
ms.sourcegitcommit: fcb27d6a46cd544feef34f6ec7607bdd46b0c12b
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/18/2020
ms.locfileid: "3146333"
---
# <a name="set-up-accessorial-assignments"></a>付帯サービス割り当ての設定

[!include [banner](../../includes/banner.md)]

この手順では、付帯サービスの割り当てを設定する方法を示します。 この設定は、通常、配送コーディネーターにより実行されます。 このガイドを使用する前に、「ハブ付帯請求金額および付帯サービス マスターの設定」ガイドを実行する必要があります。


## <a name="set-up-accessorial-assignment"></a>付帯サービス割り当ての設定
1. [輸送管理] > [設定] > [評価] > [付帯サービス割り当て] に移動します。
2. [新規] をクリックします。
3. [名前] フィールドに値を入力します。
4. [詳細] セクションの展開を切り替えます。
5. [ハブ] フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。
6. 一覧で、「ハブ付帯請求金額および付帯サービス マスターの設定」ガイドを実行し、付帯サービス マスターを作成したときに使用したハブを選択します。 
7. [ハブ付帯サービス ID] フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。
8. 一覧で、選択された行のリンクをクリックします。
9. [基準] セクションの展開を切り替えます。
    * 条件セクションでは、ここで提供される異なる値に基づいて、請求金額が適用される日付を特定するための正確な条件を選択できます。  
10. [常に適用する] オプションをオンに設定します。
11. [付帯サービス割り当てレベル] フィールドで、オプションを選択します。
12. [計算] セクションの展開を切り替えます。
13. [付帯サービス手数料タイプ] フィールドで、「一律」を選択します。
    * 付帯サービス手数料タイプによって実際の請求金額の計算方法が特定されます。 この例では、一律手数料です。  
14. [付帯サービス手数料タイプ] フィールドに数値を入力します。
15. [保存] をクリックします。

