---
title: サービス注文の手動作成
description: サービス契約または **サービス注文** フォームを使用すると、サービス注文を手動で作成することができます。
author: ShylaThompson
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SMAServiceOrderTable, SMAAgreementTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 486b4a0291ca527e647c9b5a41ff2e65a7820291
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/01/2021
ms.locfileid: "5817584"
---
# <a name="create-service-orders-manually"></a>サービス注文の手動作成    

[!include [banner](../includes/banner.md)]


サービス契約または **サービス注文** フォームを使用すると、サービス注文を手動で作成することができます。 プロジェクトからサービス注文を作成することもできます。

> [!TIP]
> <P>サービス注文の作成に自動化されたプロセスを使用できます。 

## <a name="create-a-service-order-manually-from-a-service-agreement"></a>サービス契約から手動でサービス注文を作成する

1.  **サービス管理** \> **共通** \> **サービス契約** \> **サービス契約** を選択します。

2.  サービス合意を選択するか、新しいサービス合意を作成します。

3.  **作成** グループで **出荷** タブを選択し、**計画されたサービス注文** を選択して **サービス注文の作成** フォームを開きます。

## <a name="create-a-service-order-manually-in-the-service-orders-form"></a>サービス注文フォームに手動でサービス注文を作成する

1.  **サービス管理** \> **共通** \> **サービス注文** \> **サービス注文** を選択します。

2.  **新規** を選択して、新しいサービス注文を作成します。

3.  サービス注文のサービス注文明細行を作成します。

> [!NOTE]
> <P><STRONG>サービス管理パラメーター</STRONG>フォームの<STRONG>サービス契約無し注文の許可</STRONG>チェック ボックスをオンにすると、このサービス注文をサービス合意に関連付けることなく、サービス注文明細行のトランザクションを転記できます。 このチェック ボックスをオフにした場合は、サービス注文明細行を転記する前に、手動で作成したサービス注文をプロジェクトに関連付ける必要があります。</P>

## <a name="create-a-service-order-from-a-project"></a>プロジェクトからサービス注文を作成する

1.  **プロジェクト管理および会計** \> **共通** \> **プロジェクト** \> **すべてのプロジェクト** に移動します。

2.  **アクション ウィンドウ** の **プロジェクト** フォームで、**管理** タブ \> を選択し、**サービス** \> **サービス注文** の順に選択します。

3.  **サービス注文** フォームで手動でサービス注文を作成する前の手順に従います。 **プロジェクト ID** フィールドに、プロジェクトの参照を表示します。

> [!NOTE]
> <P><STRONG>サービス管理パラメーター</STRONG>フォームの<STRONG>サービス契約無し注文の許可</STRONG>チェック ボックスをオンにすると、このサービス注文をサービス合意に関連付けることなく、サービス注文明細行のトランザクションを転記できます。 このチェック ボックスをオフにした場合は、サービス注文明細行を転記する前に、手動で作成したサービス注文をプロジェクトに関連付ける必要があります。</P>

## <a name="create-a-service-order-from-the-sales-order-form"></a>販売注文フォームからサービス注文を作成する

**販売注文に基づいて新しいサービス注文を作成** ウィザードを使用して、**販売注文** フォームからサービス注文フォームを作成できます。

1.  **販売とマーケティング** \> **共通** \> **販売注文** \> **すべての販売注文** に移動します。

2.  関連する販売注文を開きます。

3.  **販売注文** タブで、**サービス注文** を選択して **販売注文に基づいて新しいサービス注文を作成** ウィザードを開始します。

4.  **次へ \>** を選択して、**サービス注文の契約の選択** ページで次の手順を完了します。
    
      - **サービス合意** フィールドを使用して、新しいサービス注文を関連付けるサービス契約を選択します。
    
      - オプション: **プロジェクト ID** フィールドを使用して、このサービス注文を特定のプロジェクトに関連付けます。

5.  **次へ \>** を選択して、**サービス注文の作成** ページで次の手順を完了します。
    
      - **優先するサービス時刻** フィールドに、サービス コールを開始する日時を入力します。
    
      - オプション: **Description** フィールドのテキストを変更します。 既定では、このフィールドには、前のページで選択したサービス契約の説明が含まれます。
    
      - **担当** フィールドで、この契約を担当する従業員の ID を選択します。顧客が希望するサービス コールの技術者の ID がわかっている場合は、その ID も選択します。
    
      - **連絡先 ID** フィールドで、このサービス注文の窓口となる、顧客企業の担当者を指定します。

6.  **次へ \>** を選択してから、**完了** を選択します。


## <a name="see-also"></a>参照

[サービス注文](service-orders.md)

[サービス注文の自動作成](create-service-orders-automatically.md)

[サービス注文の作成 (クラス フォーム)](https://technet.microsoft.com/library/aa553901\(v=ax.60\)) 



[!INCLUDE[footer-include](../../includes/footer-banner.md)]