---
title: オプションの属性を使用して XML 形式でファイルをインポートする
description: このトピックでは、XML 形式で受信する電子ドキュメントを解析するために XML 属性を指定する ER 形式のデザインについて説明します。
author: NickSelin
manager: AnnBe
ms.date: 07/03/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: EROperationDesigner
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: global
ms.author: nselin
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: eb5d721784f45097ab466f75d43256495aac36ca
ms.sourcegitcommit: 16bfa0fd08feec1647829630401ce62ce2ffa1a4
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/02/2019
ms.locfileid: "1849998"
---
# <a name="import-files-in-xml-format-with-optional-attributes"></a>オプションの属性を使用して XML 形式でファイルをインポートする

XML 形式で受信する電子ドキュメントを解析するための電子申告 (ER) 形式をデザインできます。 XML 要素の特定の属性は、デザインされた ER 形式でオプションとして指定することができます。 これにより、該当する XML 属性のある受信ファイルとない受信ファイルを正しく処理することができます。 その後、アプリケーションのデータを更新するのに、これらのファイルからの内容を使用できます。

この機能の詳細を知るには、7.5.4.3 IT サービス/ソリューション コンポーネントの取得/開発 (10677) 業務プロセスの一部である [RCS オプションの属性を使用して XML 形式のファイルをインポートする](tasks/import-files-xml-format-optional-attributes.md) トピックの手順を実行します。 このタスク ガイドおよび関連するサンプル ファイは [Microsoft ダウンロード センター](https://go.microsoft.com/fwlink/?linkid=874684) からダウンロードすることができます。


| コンテンツの説明       | ファイル                                                         |
|---------------------------|--------------------------------------------------------------|
| XML 形式のサンプル ファイル | IncomingDocumentToLearnHowToHandleOptionalAttributes.xml     |
| タスク ガイド                | RCS オプションの attributes.axtr を使用して XML 形式のファイルをインポートする |


次のステップでは、システム管理者または電子申告開発者のロールに割り当てられているユーザーが、電子申告 (ER) の形式のコンフィギュレーションをデザインし、オプションの属性を含む XML 形式のファイルをインポートする方法について説明します。 これらの手順を完了するには、まず手順の [コンフィギュレーションプロバイダーを作成し、それを有効としてマークする](tasks/er-configuration-provider-mark-it-active-2016-11.md) にある手順を完了する必要があります。 始める前に、Microsoft ダウンロード センター (https://go.microsoft.com/fwlink/?linkid=874684) から IncomingDocumentToLearnHowToHandleOptionalAttributes.xml ファイルをダウンロードし、ローカルに保存します。

1. **組織管理** > **ワークスペース** > **電子申告**の順に移動します。
2. サンプル会社 Litware, Inc. のコンフィギュレーション プロバイダーが使用可能であり、**アクティブ**としてマークされていることを確認します。 この構成プロバイダーが表示されない場合は、[構成プロバイダーの作成および有効なプロバイダーとしてのマーク付け](tasks/er-configuration-provider-mark-it-active-2016-11.md) というトピックにある手順を完了してください。
3. **コンフィギュレーションをレポートする**をクリックします。

## <a name="create-a-new-data-model-configuration"></a>新しいデータ モデル コンフィギュレーションの作成
1. **コンフィギュレーションの作成**をクリックして、ドロップ ダイアログを開きます。
2. **名前**フィールドに、「XML ファイルをインポートするモデル」と入力します。
3. **コンフィギュレーションの作成**をクリックします。
4. **デザイナー** をクリックします。
5. **新規**をクリックすると、ドロップ ダイアログが開きます。
6. **名称**のフィールドに、「Root」と入力します。
7. **追加**をクリックします。
8. **新規**をクリックすると、ドロップ ダイアログが開きます。
9. **名称**のフィールドに、「リスト」と入力します。
10. **品目タイプ** フィールドで、**レコード リスト**を選択します。
11. **追加**をクリックします。
12. **新規**をクリックすると、ドロップ ダイアログが開きます。
13. **名称**フィールドに、「コード」と入力します。
14. **品目タイプ**フィールドで、**文字列**を選択します。
15. **追加**をクリックします。
16. **保存**をクリックします。
17. ページを閉じます。
18. **状態の変更**をクリックします。
19. **完了**をクリックします。
20. **OK**をクリックします。

## <a name="create-a-format-for-data-import"></a>データ インポート用の形式の作成
1. **コンフィギュレーションの作成**をクリックして、ドロップ ダイアログを開きます。
2. **新規**フィールドで、「XML ファイルをインポートするモデルのデータ モデルに基づく形式」と入力します。
3. **名前**フィールドに、「XML ファイルをインポートする形式」と入力します。 
4. **データのインポートのサポート** フィールドで**はい**を選択します。
5. **コンフィギュレーションの作成**をクリックします。

## <a name="design-a-format-to-parse-incoming-file-in-xml-format"></a>XML 形式で受信するファイルを解析する形式のデザイン
1. **デザイナー** をクリックします。
2. **ルートの追加**をクリックして、ドロップ ダイアログを開きます。
3. ツリーで、**XML\Element** を選択します。
4. **名称**のフィールドに、「Root」と入力します。
5. **OK**をクリックします。
6. **追加**をクリックしてドロップ ダイアログを開きます。
7. ツリーで、**XML\Element** を選択します。
8. **名前**フィールドに、「ドキュメント」と入力します。
9. **多様性**フィールドで、**1 つ、多数**を選択します。
10. **OK**をクリックします。
11. ツリーで、**root\document** を選択します。
12. **追加**をクリックしてドロップ ダイアログを開きます。
13. ツリーで、**XML\Attribute** を選択します。
14. **名前**フィールドに、「ID」と入力します。
15. **OK**をクリックします。
16. **保存**をクリックします。

## <a name="design-a-format-mapping-to-save-parsed-information-to-data-model"></a>解析された情報をデータ モデルに保存する形式マッピングのデザイン
1.  **形式をモデルにマップ**をクリックします。
2.  **新規** をクリックします。
3.  **定義**フィールドで値を入力または選択します。
4.  **名前**フィールドに、「マッピング」と入力します。
5.  **保存**をクリックします。
6.  **デザイナー** をクリックします。
7.  ツリーで、**形式**を展開します。
8.  ツリーで、**format\root: XML Element(root)** を展開します。
9.  ツリーで、**format\root: XML Element(root)\document: XML Element 1* を選択します。 (ドキュメント)**。
10. **バインド**をクリックします。
11. ツリーで、**format\root: XML Element(root)\document: XML Element 1* を展開します。 (ドキュメント)**。
12. ツリーで、**format\root: XML Element(root)\document: XML Element 1* を選択します。 (ドキュメント)\id**。
13. ツリーで、**List = format.root.document** を展開します。
14. ツリーで、**List = format.root.document\Code** を選択します。
15. **バインド**をクリックします。
16. **保存**をクリックします。
17. ページを閉じます。

## <a name="run-format-mapping"></a>形式マッピングの実行
1. **実行**をクリックします。
2. **参照**をクリックし、ファイル **IncomingDocumentToLearnHowToHandleOptionalAttributes.xml** を選択します。
3. **OK** をクリックします。

> [!NOTE]
> 選択したファイルは、「document」要素に「ID」属性が存在するように想定した形式デザインとしてインポートされませんでしたが、インポートされたファイルにそのような属性は含まれていません。

## <a name="modify-format-structure-to-handle-xml-attribute-as-optional"></a>XML 属性をオプションとして処理するよう形式構造を変更
1. ページを閉じます。
2. ツリーで、**root\document** を展開します。
3. ツリーで、**root\document\id** を選択します。
4. **存在しない属性に対する空の文字列**フィールドで、**はい**を選択します。
5. **保存**をクリックします。

## <a name="run-format-mapping-to-test-changes"></a>変更をテストするための形式マッピングの実行
1. **形式をモデルにマップ**をクリックします。
2. **実行**をクリックします。
3. **参照**をクリックし、ファイル **IncomingDocumentToLearnHowToHandleOptionalAttributes.xml** を選択します。
4. **OK** をクリックします。
5. 生成したファイルを確認します。 同じファイルが形式デザインとしてインポートされて、「document」要素の「ID」属性はオプションとして見なされることに注意してください。
