---
title: サービス BOM の変更
description: サービス BOM を変更します。
author: sorenva
ms.date: 05/03/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SMAAgreementTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: sorenand
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c0aac9bf0f312052160b29be606ba587f2de0184
ms.sourcegitcommit: cfe8fbc202c3eb05d894076fdf99e46704f17365
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/15/2022
ms.locfileid: "9014669"
---
# <a name="modify-a-service-bom"></a>サービス BOM の変更 

[!include [banner](../includes/banner.md)]


サービス BOM 内の要素の履歴を記録できます。 BOM 明細行を更新するたびに、履歴行が **履歴** ウィンドウ内に作成されます。 履歴行には、BOM 明細行の現在のステータスが表示されます。

## <a name="update-a-service-bom-element"></a>サービス BOM 要素の更新

1.  **サービス管理** \> **サービス契約** \> **サービス契約** をクリックします。

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

1.  **サービス管理** \> **サービス契約** \> **サービス契約** をクリックします。

2.  **編集** をクリックして **サービス合意** 詳細フォームを開きます。

3.  **アクション ウィンドウ** で、**サービス対象** をクリックして **サービス対象** フォームを開くきます。

4.  サービス BOM 明細行を削除する対象を選択し、**デザイナ** をクリックします。

5.  **デザイナ** フォームで、削除する BOM 明細行を選択し、**BOM 明細行の削除** をクリックします。

## <a name="see-also"></a>参照

[テンプレート BOM](template-boms.md)

  




[!INCLUDE[footer-include](../../includes/footer-banner.md)]