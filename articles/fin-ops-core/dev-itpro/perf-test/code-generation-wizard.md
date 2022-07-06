---
title: 受け入れテスト ライブラリ コード生成ウィザード
description: この記事では、受け入れテスト ライブラリのコード生成ウィザードに関する情報を提供します。
author: MichaelFruergaardPontoppidan
ms.date: 03/27/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Developer
ms.reviewer: tfehr
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mfp
ms.search.validFrom: 2019-03-27
ms.dyn365.ops.version: App Update 10.0.2
ms.openlocfilehash: 35ce163652366c47fa7f1ed5eddcc1676da4e901
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/03/2022
ms.locfileid: "8862134"
---
# <a name="acceptance-test-library-code-generation-wizard"></a>受け入れテスト ライブラリ コード生成ウィザード

[!include [banner](../includes/banner.md)]

引受テスト ライブラリ (ATL) コード ジェネレーターはすばやくを生成し、新しいATLエンティティ、クエリ、およびテーブルとデータ エンティティに基づく仕様を更新します。

## <a name="create-the-atlentity-class-by-using-the-wizard"></a>ウィザードを使用して、AtlEntityクラスを作成します。

`AtlEntity` クラスを作成するには、以下の手順に従って **コード生成** ウィザードを使用します。

1. Microsoft Visual Studioを起動し、デザイナー ウィンドウで、テーブルを開きます。
2. テーブルの名前を右クリックし、 **アドイン** メニューで、 **ATLエンティティの生成** を選択します。
3. `AtlEntity` クラスに含めるフィールドを選択し、 **追加** を選択します。
4. 必要に応じてエンティティとフィールド名称を変更します。
5. **生成** を選択してクラスを作成します。

### <a name="additional-optional-steps"></a>追加オプション

`AtlEntity` クラスを作成する際に、以下の作業を同時に実行するができます。

- シナリオに必要なアクションを追加します。
- `default` メソッドを `AtlData` クラスに追加する。
- `setMainRecordField` メソッドを上書きし、テーブル上の `modifiedField(_fieldId)` メソッドを呼び出す。

    ```xpp
    protected void setMainRecordField(FieldId _fieldId, anytype _value)
    {
        super(_fieldId, _value);
        common.modifiedField(_fieldId);
    }
    ```

## <a name="create-the-atlquery-class-by-using-the-wizard"></a>ウィザードを使用して、AtlQueryクラスを作成します。

`AtlQuery` クラスを作成するには、以下の手順に従って **コード生成** ウィザードを使用します。

1. Microsoft Visual Studioを起動し、デザイナー ウィンドウで、テーブルを開きます。
2. テーブルの名前を右クリックし、 **アドイン** メニューで、 **ATLエンティティの生成** を選択します。
3. `AtlQuery` クラスに含めるフィールドと関連付けを選択し、 **追加** を選択します。
4. 必要に応じてクエリ、フィールド名称、関連付けの名称を変更します。
5. **生成** を選択してクラスを作成します。

### <a name="additional-optional-steps"></a>追加オプション

`AtlQuery` クラスを作成する際に、`query` のメソッドを `AtlData` のクラスに追加することが可能です。 これにより、この記事の最初に作成した `AtlQuery` クラスのインスタンスを返します。

## <a name="create-the-atlspec-class-by-using-the-wizard"></a>ウィザードを使用して、AtlSpecクラスを作成します。

`AtlSpec` クラスを作成するには、以下の手順に従って **コード生成** ウィザードを使用します。

1. Microsoft Visual Studioを起動し、デザイナー ウィンドウで、テーブルを開きます。
2. テーブルの名前を右クリックし、 **アドイン** メニューで、 **ATL Specificationの生成** を選択します。
3. `AtlSpec` クラスに含めるフィールドを選択し、 **追加** を選択します。
4. 必要に応じてSpecificationとフィールド名称を変更します。
5. **生成** を選択してクラスを作成します。

### <a name="additional-optional-steps"></a>追加オプション

`spec` のメソッドをデータ クラスに追加することにより、この記事の最初に作成した `AtlSpec` クラスのインスタンスを返します。


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]