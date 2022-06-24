---
title: ビジネス ドキュメント テンプレートの構造の更新
description: この記事では、ビジネス ドキュメント管理機能を使用して、ビジネス ドキュメント テンプレートの構造を更新する方法について説明します。
author: NickSelin
ms.date: 11/19/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ERBDWorkspace, ERBDParameters, ERBDTemplateEditor
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2019-12-01
ms.dyn365.ops.version: 10.0.9
ms.openlocfilehash: 2adecba4e988bfe04de2c181501b6c3ef8491dcf
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/03/2022
ms.locfileid: "8880286"
---
# <a name="update-the-structure-of-a-business-document-template"></a>ビジネス ドキュメント テンプレートの構造の更新 

[!include[banner](../includes/banner.md)]

[ビジネス ドキュメント管理](er-business-document-management.md) テンプレート エディターの **テンプレート構造** ペインで 、Microsoft Excel のテンプレートに [新しいフィールドを追加](er-bdm-add-field-to-excel-template.md) することによって、ビジネス ドキュメント テンプレートを変更できます。 テンプレートの構造が Dynamics 365 Finance で自動的に更新されるので、**テンプレート構造** ペインで行った変更が反映されます。

Office 365 オンライン機能を使用してテンプレートを変更することもできます。 たとえば、画像や図形などの新しい名前付きの項目を編集可能なワークシートに追加できます。 この場合、財務でテンプレートの構造が自動的に更新されず、追加した項目は **テンプレート構造** ペインに表示されません。 テンプレート エディター ページの **構造の更新** を選択して、Finance のテンプレート構造を手動で更新します。

この機能の詳細については、次の例を実行します。

## <a name="example-update-the-structure-of-a-business-document-template"></a>例: ビジネス ドキュメント テンプレートの構造の更新

この例では、Office Online でテンプレートを変更した後に、システム管理者が Finance でビジネス ドキュメント テンプレートの構造を更新する方法を示します。 以降のセクションでは、関連する手順について説明します。

### <a name="prepare-a-business-document-template-for-editing"></a>編集用のビジネス ドキュメント テンプレートの準備

[ビジネス ドキュメント管理の概要](er-business-document-management.md) で、次の手順を実行します。

1. [ER パラメーターの構成](er-business-document-management.md#configure-er-parameters)
2. [ER ソリューションのインポート](er-business-document-management.md#import-er-solutions)
3. [ビジネス ドキュメント管理の有効](er-business-document-management.md#enable-business-document-management)
4. [パラメータのコンフィギュレーション](er-business-document-management.md#configure-parameters)

### <a name="edit-a-business-document-template"></a>ビジネス ドキュメント テンプレートの編集

1. **ビジネス ドキュメント管理** ワークスペースで、**新規ドキュメント** を選択します。
2. **新しいテンプレートの作成** ページで、**自由書式の請求書 (ER サンプル)(Excel)** テンプレートを選択します。
3. **ドキュメントの作成** を選択します。
4. **タイトル** フィールドに、**FTI サンプル Litware** と入力します。
5. **OK** を選択して、新しいテンプレートを作成します。

    > [!NOTE]
    > Office Online にまだサインインしていない場合は、[Office 365 サインイン ページに移動](er-business-document-management.md#frequently-asked-questions) します。 Finance 環境に戻るには、ブラウザーの **戻る** ボタンを選択します。

    新しいテンプレートが、テンプレート エディター ページの Excel Online 埋め込みコントロールで編集するために開かれます。

[![ビジネス ドキュメント管理ワークスペースを使用して、ビジネス ドキュメント テンプレートの編集を開始する。](./media/er-bdm-update-structure1.gif)](./media/er-bdm-update-structure1.gif)

### <a name="review-the-current-structure-of-the-editable-template"></a>編集可能なテンプレートの現在の構造の確認

1. Excel Online のリボンにある **表示** タブの **表示** グループで、**グリッド線** を選択します。
2. 編集可能なテンプレートで、テンプレート タイトルの上の四角形を選択します。 この四角形は、**rptHeaderCompLogo** という名前の画像になります。
3. **テンプレート構造** ペインが非表示になっている場合は、**構造を表示** を選択します。
4. **テンプレート構造** ペインで、**レポート \> 請求書 \> rptHeader \> rptHeaderPart1** の順に展開します。
5. Finance のテンプレート構造では、**rptHeaderCompLogo** 項目が、**レポート \> 請求書 \> rptHeader \> rptHeaderPart1** の子項目として表示されていることに注意してください。

[![ビジネス ドキュメント 管理ワークスペースを使用して編集可能なテンプレートの現在の構造を確認する。](./media/er-bdm-update-structure2.gif)](./media/er-bdm-update-structure2.gif)

### <a name="update-the-structure-of-a-business-document-template-by-deleting-a-picture"></a>画像を削除して、ビジネス ドキュメント テンプレートの構造を更新する

1. Excel Online の編集可能なテンプレートで、**rptHeaderCompLogo** の画像を選択します。
2. 次のいずれかの手順に従って、編集可能なテンプレートから選択した画像を削除します:

    - キーボードの **Delete** キーを選択します。
    - 画像を選択したまま (または右クリック) にして、**切り取り** を選択します。

    > [!NOTE]
    > **rptHeaderCompLogo** 項目は、画像が Excel テンプレートに含まれない場合でも、Finance のテンプレート構造に現在も存在しています。

3. **構造の更新** を選択し、Excel および Finance で編集可能なテンプレートの構造を同期します。
4. **テンプレート構造** ペインで、**レポート \> 請求書 \> rptHeader \> rptHeaderPart1** の順に展開します。
5. **rptHeaderCompLogo** 項目が Finance のテンプレート構造に含まれていないことに注意してください。

[![ビジネス ドキュメント管理ワークスペースを使用して、ビジネス ドキュメント テンプレートから画像を削除する。](./media/er-bdm-update-structure3.gif)](./media/er-bdm-update-structure3.gif)

### <a name="update-the-structure-of-a-business-document-template-by-adding-a-picture"></a>画像を追加して、ビジネス ドキュメント テンプレートの構造を更新する

1. Excel Online のリボンにある **挿入** タブの **図** グループで、**画像** を選択します。
2. **ファイルの選択** を選択し、追加するイメージを参照して選択し、**OK** を選択します。
3. **挿入** を選択します。
4. 新しい画像を正しい位置になるまで移動します。 既定では、Excel が画像に名前を付けます。 たとえば、画像に **画像 2** という名前を付けます。
5. **構造の更新** を選択し、Excel および Finance で編集可能なテンプレートの構造を同期します。
6. **テンプレート構造** ペインで、**レポート \> 請求書 \> rptHeader \> rptHeaderPart1** の順に展開します。
7. 新しい画像が Finance のテンプレート構造の項目として含まれていることに注意してください。

[![ビジネス ドキュメント管理ワークスペースを使用して、ビジネス ドキュメント テンプレートに画像を追加する。](./media/er-bdm-update-structure4.gif)](./media/er-bdm-update-structure4.gif)

## <a name="related-links"></a>関連リンク

[電子申告 (ER) の概要](general-electronic-reporting.md)

[ビジネス ドキュメント管理の概要](er-business-document-management.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]