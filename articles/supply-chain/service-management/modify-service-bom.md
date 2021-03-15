---
title: サービス BOM の変更
description: サービス BOM を変更します。
author: ShylaThompson
manager: tfehr
ms.date: 05/03/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMAAgreementTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c69f575dae369350e3191c31f961a861dea0fb07
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/15/2021
ms.locfileid: "4996554"
---
# <a name="modify-a-service-bom"></a>サービス BOM の変更 

[!include [banner](../includes/banner.md)]


サービス BOM 内の要素の履歴を記録できます。 BOM 明細行を更新するたびに、履歴行が **履歴** ウィンドウ内に作成されます。 履歴行には、BOM 明細行の現在のステータスが表示されます。

## <a name="update-a-service-bom-element"></a>サービス BOM 要素の更新

1.  **サービス管理** \> **共通** \> **サービス契約** \> **サービス契約** の順にクリックします。

2.  **編集** をクリックして **サービス合意** 詳細フォームを開きます。

3.  **アクション ウィンドウ** で、**サービス対象** をクリックして **サービス対象** フォームを開くきます。

4.  BOM 明細行を更新する対象を選択し、**デザイナ** をクリックします。

5.  **デザイナ** フォームで、更新する BOM 明細行を選択し、**BOM 明細行の編集** をクリックします。
    
    > [!NOTE]
    > <P>明細行をサービス BOM にドラッグする際に<STRONG>BOM 明細行の編集</STRONG>フォームを開く場合、<STRONG>設定</STRONG>タブで、<STRONG>追加時に編集</STRONG>チェック ボックスをオンにします。</P>

6.  **数量** フィールドで、数量を入力します。

7.  請求できる交換品目のサービス注文明細行を作成する場合は、**サービス注文明細行の作成** チェック ボックスをオンにします。

8.  **OK** をクリックしてフォームを閉じます。

## <a name="delete-a-service-bom-line"></a>サービス BOM 明細行の削除

1.  **サービス管理** \> **共通** \> **サービス契約** \> **サービス契約** の順にクリックします。

2.  **編集** をクリックして **サービス合意** 詳細フォームを開きます。

3.  **アクション ウィンドウ** で、**サービス対象** をクリックして **サービス対象** フォームを開くきます。

4.  サービス BOM 明細行を削除する対象を選択し、**デザイナ** をクリックします。

5.  **デザイナ** フォームで、削除する BOM 明細行を選択し、**BOM 明細行の削除** をクリックします。

## <a name="see-also"></a>参照

[テンプレート BOM](template-boms.md)

  




[!INCLUDE[footer-include](../../includes/footer-banner.md)]