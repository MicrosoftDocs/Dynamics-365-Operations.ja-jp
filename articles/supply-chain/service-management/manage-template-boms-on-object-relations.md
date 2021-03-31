---
title: 対象関係でのテンプレート BOM の管理
description: 対象関係でテンプレート BOM を管理します。
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
ms.openlocfilehash: 3b4b615ab1df5031afe52d3392d76c8da386dd8e
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/15/2021
ms.locfileid: "5204427"
---
# <a name="manage-template-boms-on-object-relations"></a>対象関係でのテンプレート BOM の管理 

[!include [banner](../includes/banner.md)]


## <a name="attach-a-template-bom-to-a-service-object"></a>テンプレート BOM のサービス対象への関連付け

1.  **サービス管理** \> **共通** \> **サービス契約** \> **サービス契約** の順にクリックします。

2.  テンプレート BOM を対象のリレーションに関連付けるサービス契約をダブルクリックします。

3.  **設定** \> **サービス対象** をクリックします。

4.  **サービス対象** フォームで、テンプレート BOM に関連付ける対象を選択し、**機能** \> **テンプレート BOM の添付** をクリックします。

5.  **テンプレート BOM を選択** ダイアログ ボックスでテンプレート BOM を選択し、**OK** をクリックします。

6.  フォームを閉じて、変更を保存します。

## <a name="delete-a-service-bom-from-a-service-object"></a>サービス BOM のサービス対象からの削除

1.  **サービス管理** \> **共通** \> **サービス契約** \> **サービス契約** の順にクリックします。

2.  サービス BOM を対象のリレーションから削除するサービス契約をダブルクリックします。

3.  **設定** \> **サービス対象** をクリックします。

4.  **サービス対象** フォームで、削除するサービス BOM を含むサービス対象を選択し、**機能** \> **サービス BOM の削除** をクリックします。

5.  フォームを閉じて、変更を保存します。

## <a name="move-the-service-bom-history-from-one-service-agreement-to-another"></a>サービス BOM 履歴のサービス合意間での移動

1.  **サービス管理** \> **共通** \> **サービス契約** \> **サービス契約** の順にクリックします。

2.  サービス BOM の移動元のサービス契約をダブルクリックします。

3.  **設定** \> **サービス対象** をクリックします。

4.  **サービス対象** フォームで、移動するサービス BOM を含むサービス対象を選択し、**機能** \> **サービス BOM の移動** をクリックします。

5.  **サービス対象関係** フォームで、サービス BOM の移動先のサービス対象リレーションを選択し、**OK** をクリックします。

6.  フォームを閉じて、変更を保存します。

## <a name="modify-the-information-displayed-for-a-bom-line"></a>BOM 明細行に表示される情報の変更

1.  **サービス管理** \> **設定** \> **サービス対象** \> **テンプレート BOM** の順にクリックします。

2.  テンプレート BOM を選択し、**デザイナ** をクリックします。

3.  **設定** タブをクリックします。**BOM** 領域で、サービス BOM およびテンプレート BOM の BOM 明細行に表示する情報のチェック ボックスをオンにします。

4.  フォームを閉じて、変更を保存します。

## <a name="see-also"></a>参照

[サービス BOM の削除](delete-service-bom.md)

  




[!INCLUDE[footer-include](../../includes/footer-banner.md)]