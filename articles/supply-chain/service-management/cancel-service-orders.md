---
title: サービス注文のキャンセル
description: サービス注文自体からサービス注文またはサービス注文明細行をキャンセルしたり、定期処理ジョブを実行して複数のサービス注文をキャンセルしたりできます。
author: ShylaThompson
manager: tfehr
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMAServiceOrderTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: b60feec05e923c25e0f0bacb28b510906d5f73cd
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/15/2021
ms.locfileid: "4974689"
---
# <a name="cancel-service-orders"></a>サービス注文のキャンセル   

[!include [banner](../includes/banner.md)]


サービス注文自体からサービス注文またはサービス注文明細行をキャンセルしたり、定期処理ジョブを実行して複数のサービス注文をキャンセルしたりできます。


> [!NOTE]
> <P>サービス注文のステージでキャンセルが許可されない場合、サービス注文に在庫品目要求がある場合、またはサービス注文が既に転記されている場合は、サービス注文をキャンセルできません。</P>


## <a name="cancel-a-service-order-in-the-service-orders-form"></a>"サービス注文" フォームでのサービス注文のキャンセル

1.  **サービス管理** \> **共通** \> **サービス注文** \> **サービス注文** の順にクリックします。 サービス注文を選択し、アクション ウィンドウで、**注文のキャンセル** をクリックします。

## <a name="cancel-a-service-order-line"></a>サービス注文明細行のキャンセル

1.  **サービス管理** \> **共通** \> **サービス注文** \> **サービス注文** の順にクリックします。 キャンセルする明細行が含まれているサービス注文をダブルクリックします。

2.  キャンセルするサービス注文明細行を選択し、**注文明細行のキャンセル** をクリックして明細行のステータスを **キャンセル済** に変更します。


> [!TIP]
> <P>サービス注文明細行のキャンセルを取り消し、ステータスを<STRONG>作成済</STRONG>に戻すには、<STRONG>キャンセルの無効化</STRONG>をクリックします。</P>


## <a name="cancel-multiple-service-orders"></a>複数のサービス注文のキャンセル

1.  **サービス管理** \> **定期処理** \> **サービス注文** \> **サービス注文のキャンセル** の順にクリックします。

2.  **選択** ボタンをクリックします。

3.  **照会** フォームの、**基準** 列で、キャンセルするサービス注文を選択します。

4.  **OK** をクリックして **照会** フォームを閉じます。

5.  キャンセルされたサービス注文を一覧表示する情報ログを生成するには、**情報ログの表示** チェック ボックスをオンにします。

6.  サービス注文の **キャンセル済** ステータスを元に戻すには、**キャンセルの無効化** チェック ボックスをオンにします。

7.  **OK** をクリックします。

選択したサービス注文がキャンセルされるか、その **キャンセル済** 進捗状況ステータスが **処理中** に戻ります。


> [!NOTE]
> <P><STRONG>キャンセルの無効化</STRONG>チェック ボックスをオンにすると、進捗状況ステータスが<STRONG>キャンセル済</STRONG> のサービス注文が取り消されて、進捗状況ステータスが<STRONG>処理中</STRONG>のサービス注文のキャンセルは実行されません。</P>


  




[!INCLUDE[footer-include](../../includes/footer-banner.md)]