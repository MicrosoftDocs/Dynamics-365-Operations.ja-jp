---
title: テンプレート BOM の作成
description: テンプレート BOM はさまざまな方法を使用して作成できます。
author: kamaybac
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SMATemplateBOMTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c10bf5e758a1752e1c50c602db85e0c53ee3e662
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/29/2021
ms.locfileid: "7571500"
---
# <a name="create-a-template-bom"></a>テンプレート BOM の作成   

[!include [banner](../includes/banner.md)]


テンプレート BOM は次のいずれかの方法を使用して作成できます。 すべての方法において、**開始日** および **終了日** フィールドは省略可能であり、情報提供のみを目的としています。

## <a name="create-a-template-bom-manually"></a>テンプレート BOM を手動で作成する

1.  **サービス管理** \> **設定** \> **サービス対象** \> **テンプレート BOM** に移動します。

2.  **新規** を選択すると **テンプレート BOM の作成** フォームが開きます。

3.  **参照から BOM 明細行をコピー** の下で、**手動** オプションを選択します。

4.  **品目番号** フィールドで、タイプ **BOM** の品目を入力します。

5.  **名前** フィールドに、テンプレートの名前を入力します。

6.  **開始日** および **終了日** フィールドに、テンプレート BOM を有効にする日付範囲を入力します。

7.  **OK** を選択します。

新しい、空のテンプレート BOM が作成されます。

## <a name="create-a-template-bom-based-on-another-template-bom"></a>別のテンプレート BOM に基づいてテンプレート BOM を作成する

1.  **サービス管理** \> **設定** \> **サービス対象** \> **テンプレート BOM** を選択します。

2.  **新規** を選択すると **テンプレート BOM の作成** フォームが開きます。

3.  **参照から BOM 明細行をコピー** の下で、**テンプレート BOM** オプションを選択します。

4.  **参照番号** フィールドで、新しいテンプレート BOM にコピーする既存のテンプレート BOM を選択します。

5.  **名前** フィールドに、テンプレートの名前を入力します。

6.  **開始日** および **終了日** フィールドに、テンプレート BOM を有効にする日付範囲を入力します。

7.  **OK** を選択します。

元のテンプレート BOM の明細行に対応する明細行を使用する、新しいテンプレート BOM が作成されます。

## <a name="create-a-template-bom-based-on-an-item-bom"></a>品目 BOM に基づいてテンプレート BOM を作成する

1.  **サービス管理** \> **設定** \> **サービス対象** \> **テンプレート BOM** を選択します。

2.  **新規** を選択すると **テンプレート BOM の作成** フォームが開きます。

3.  **参照から BOM 明細行をコピー** の下で、**BOM** を選択します。

4.  **参照番号** フィールドで、BOM バージョンを選択します。 BOM タイプの品目が **品目番号** にコピーされます。

5.  **名前** フィールドに、テンプレートの名前を入力します。

6.  **開始日** および **終了日** フィールドに、テンプレート BOM を有効にする日付範囲を入力します。

7.  **OK** を選択します。

**部品表** に表示された BOM の明細行に対応する明細行を使用して、新しいテンプレート BOM が作成されます。

## <a name="create-a-template-bom-based-on-a-production-bom"></a>生産 BOM に基づいてテンプレート BOM を作成する

1.  **サービス管理** \> **設定** \> **サービス対象** \> **テンプレート BOM** を選択します。

2.  **新規** を選択すると **テンプレート BOM の作成** フォームが開きます。

3.  **参照から BOM 明細行をコピー** の下で、**生産** を選択します。

4.  **参照番号** フィールドで、生産 BOM を選択します。

5.  **名前** フィールドに、テンプレートの名前を入力します。

6.  **開始日** および **終了日** フィールドに、テンプレート BOM を有効にする日付範囲を入力します。

7.  **OK** を選択します。

**BOM** に表示された BOM の明細行に対応する明細行を使用して、新しいテンプレート BOM が作成されます。

## <a name="see-also"></a>参照

[テンプレート BOM](template-boms.md)

  




[!INCLUDE[footer-include](../../includes/footer-banner.md)]