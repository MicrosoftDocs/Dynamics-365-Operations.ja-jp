---
title: (RCS) オプションの属性を使用して XML 形式のファイルをインポートする
description: この記事では、オプションの属性を含む XML 形式のファイルをインポートするため、ユーザーが ER 形式構成をデザインする方法を説明します。
author: kfend
ms.date: 07/01/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: filatovm
ms.search.validFrom: 2019-07-28
ms.dyn365.ops.version: Version 7.0.0
ms.search.form: ''
ms.openlocfilehash: 5254a3d631129d0e41fcd37a341b54f97cfe6a9e
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/12/2022
ms.locfileid: "9290007"
---
# <a name="rcs-import-files-in-xml-format-with-optional-attributes"></a>(RCS) オプションの属性を使用して XML 形式のファイルをインポートする

[!include [banner](../../includes/banner.md)]

次のステップでは、システム管理者または電子申告開発者のロールに割り当てられているユーザーが、電子申告 (ER) の形式のコンフィギュレーションをデザインし、オプションの属性を含む XML 形式のファイルをインポートする方法について説明します。 この手順を完了するには、まず 「構成プロバイダーを作成し、有効としてマークする」 に記載の手順を完了する必要があります。 始める前に、[Microsoft ダウンロードセンター](https://go.microsoft.com/fwlink/?linkid=874684) から IncomingDocumentToLearnHowToHandleOptionalAttributes.xml ファイルをダウンロードし、ローカルに保存します。

1.    **すべてのワークスペース** > **電子申告** の順に移動します。
2.    サンプル会社 Litware, Inc. のコンフィギュレーション プロバイダーが使用可能であり、**アクティブ** としてマークされていることを確認します。 このコンフィギュレーション プロバイダーが表示されない場合は、[コンフィギュレーション プロバイダーを作成し、有効としてマークする](er-configuration-provider-mark-it-active-2016-11.md) という手順のステップを完了する必要があります。
3.    **コンフィギュレーションをレポートする** をクリックします。

## <a name="create-a-new-data-model-configuration"></a>新しいデータ モデル コンフィギュレーションの作成
1.    **コンフィギュレーションの作成** をクリックして、ドロップ ダイアログを開きます。
2.    **名前** フィールドに、「XML ファイルをインポートするモデル」と入力します。
3.    **コンフィギュレーションの作成** をクリックします。
4.    **デザイナー** をクリックします。
5.    **新規** をクリックすると、ドロップ ダイアログが開きます。
6.    **名称** のフィールドに、「Root」と入力します。
7.    **追加** をクリックします。
8.    **新規** をクリックすると、ドロップ ダイアログが開きます。
9.    **名称** のフィールドに、「リスト」と入力します。
10.    **品目タイプ** フィールドで、**レコード リスト** を選択します。
11.    **追加** をクリックします。
12.    **新規** をクリックすると、ドロップ ダイアログが開きます。
13.    **名称** フィールドに、「コード」と入力します。
14.    **品目タイプ** フィールドで、**文字列** を選択します。
15.    **追加** をクリックします。
16.    **保存** をクリックします。
17.    ページを閉じます。
18.    **状態の変更** をクリックします。
19.    **完了** をクリックします。
20.    **OK** をクリックします。

## <a name="create-a-format-for-data-import"></a>データ インポート用の形式の作成
1.    **コンフィギュレーションの作成** をクリックして、ドロップ ダイアログを開きます。
2.    **新規** フィールドで、「XML ファイルをインポートするモデルのデータ モデルに基づく形式」と入力します。
3.    **名前** フィールドに、'xml ファイルをインポートする形式' と入力します。
4.    **データのインポートのサポート** フィールドで **はい** を選択します。
5.    **コンフィギュレーションの作成** をクリックします。

## <a name="design-a-format-to-parse-incoming-file-in-xml-format"></a>XML 形式で受信するファイルを解析する形式のデザイン
1.    **デザイナー** をクリックします。
2.    **ルートの追加** をクリックして、ドロップ ダイアログを開きます。
3.    ツリーで、**XML\Element** を選択します。
4.    **名称** のフィールドに、「Root」と入力します。
5.    **OK** をクリックします。
6.    **追加** をクリックしてドロップ ダイアログを開きます。
7.    ツリーで、**XML\Element** を選択します。
8.    **名前** フィールドに、「ドキュメント」と入力します。
9.    **多様性** フィールドで、**1 つ、多数** を選択します。
10.    **OK** をクリックします。
11.    ツリーで、**root\document** を選択します。
12.    **追加** をクリックしてドロップ ダイアログを開きます。
13.    ツリーで、**XML\Attribute** を選択します。
14.    **名前** フィールドに、'ID' と入力します。
15.    **OK** をクリックします。
16.    **保存** をクリックします。

## <a name="design-a-format-mapping-to-save-parsed-information-to-data-model"></a>解析された情報をデータ モデルに保存する形式マッピングのデザイン
1. **形式をモデルにマップ** をクリックします。
2. **新規** をクリックします。
3. **定義** フィールドで値を入力または選択します。
4. 一覧で、選択された行のリンクをクリックします。
5. **名前** フィールドに、「マッピング」と入力します。
6. **保存** をクリックします。
7. **デザイナー** をクリックします。
8. ツリーで、**形式** を展開します。
9. ツリーで、**format\root: XML Element(root)** を展開します。
10.    ツリーで、**format\root: XML Element(root)\document: XML Element 1* を選択します。 (ドキュメント)**。
11.    **バインド** をクリックします。
12.    ツリーで、**format\root: XML Element(root)\document: XML Element 1* を展開します。 (ドキュメント)**。
13.    ツリーで、**format\root: XML Element(root)\document: XML Element 1* を選択します。 (ドキュメント)\id**。
14.    ツリーで、**List = format.root.document** を展開します。
15.    ツリーで、**List = format.root.document\Code** を選択します。
16.    **バインド** をクリックします。
17.    **保存** をクリックします。
18.    ページを閉じます。
 
## <a name="run-format-mapping"></a>形式マッピングの実行
1. **実行** をクリックします。
2. **参照** をクリックし、**IncomingDocumentToLearnHowToHandleOptionalAttributes.xml** を選択します。
3. **OK** をクリックします。

> [!NOTE]
> 選択したファイルは、「document」要素に「ID」属性が存在するように想定した形式デザインとしてインポートされませんでしたが、インポートされたファイルにそのような属性は含まれていません。

## <a name="modify-format-structure-to-handle-xml-attribute-as-optional"></a>XML 属性をオプションとして処理するよう形式構造を変更
1. ページを閉じます。
2. ツリーで、**root\document** を展開します。
3. ツリーで、**root\document\id** を選択します。
4. **存在しない属性に対する空の文字列** フィールドで、**はい** を選択します。
5. **保存** をクリックします。
 
## <a name="run-format-mapping-to-test-changes"></a>変更をテストするための形式マッピングの実行
1. **形式をモデルにマップ** をクリックします。
2. **実行** をクリックします。
3. **参照** をクリックし、**IncomingDocumentToLearnHowToHandleOptionalAttributes.xml** ファイルを選択します。
4. **OK** をクリックします。
5. 生成したファイルを確認します。 

> [!NOTE]
> 同じファイルがフォーマット デザインとしてインポートされて、‘document’ 要素の ‘ID’ 属性はオプションとして見なされます。


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
