---
title: ルックアップ コントロール
description: この記事では、コントロールの検索動作を有効にする方法について説明します。
author: jasongre
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Developer
ms.reviewer: rhaertle
ms.custom: 17464
ms.assetid: 1c71ebac-47c3-4c7e-bb48-a1c45619c95e
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 3d650b9f8db1be06ea71c0e06391d99d04987a20
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/31/2021
ms.locfileid: "5751332"
---
# <a name="lookup-controls"></a>ルックアップ コントロール

[!include [banner](../includes/banner.md)]

この記事では、コントロールの検索動作を有効にする方法について説明します。 また、複数選択ルックアップを作成する方法について説明し、現在サポートされていないルックアップ シナリオの概要について説明します。

<a name="enabling-lookup-behavior-in-controls"></a>コントロールのルックアップ動作を有効化
------------------------------------

### <a name="controls-bound-to-an-extended-data-type"></a>拡張データ型にバインドされたコントロール

拡張データ型プロパティ セット (実行中の FormDataSource が無い) を持つコントロールは、次の条件の下で検索を行います。

1.  EDT にはそのテーブル リレーションまたはテーブルの参照ノードが設定されているかどうか。
2.  FormHelp プロパティが設定されている場合、ルール \#1 を true に設定 (カスタム ルックアップ) する必要はありません。
3.  コントロールでルックアップまたは lookupReference が上書きされている場合。 このルールは、完全な非連結コントロール (EDT、フィールド、またはデータ メソッドなし) にも適用されることに注意してください。 これには、registerOverrideMethod などの上書きも含まれます。

### <a name="controls-bound-to-a-form-data-source"></a>フォーム データ ソースにバインドされたコントロール

データ ソースにバインドされたコントロールは、次の条件の下で検索されます。**フィールド バインド**

1.  "lookup" または "lookupReference" (参照コントロール) メソッドが上書きされます。
    1.  FormDataSource フィールドでルックアップまたは lookupReference が上書きされている場合。
    2.  コントロールでルックアップまたは lookupReference が上書きされている場合。
        -   これには、registerOverrideMethod などの上書きも含まれます。

2.  このフィールドに EDT がある場合、「拡張データ型にバインドされたコントロール」セクションのルール \# が適用されます。
3.  バインディング フィールドは、DBFGetRef ルールごとにリレーションをマップします。
    1.  高レベルのルール。
        1.  フィールドを支持する EDT 関係が存在し、テーブル関係ノードが入力され、Ignore EDT Relations がフィールド上で false である場合、その関係が使用されます (ルックアップがある)。
        2.  フィールドに対してリレーション マッピングが使用され、任意の固定フィールド リンク条件が満たされている場合は、そのリレーションが使用されます (ルックアップがある)。
            1.  検証は「はい」にする必要があります。

        3.  次の場合に発生する 移行された EDT 関係の特殊なケースに注意してください。
            1.  フィールドは、関係ノードが設定される EDT によってサポートされます。
            2.  フィールドは、「EDTRelation」設定を「はい」にするテーブル関係によってサポートされます。
            3.  テーブル関係リンクは SourceEDT が適切な EDT に設定されています。

        4.  また、IgnoreEDTRelation がフィールド上で true にセットされているケースを持つことができます。このケースでは、このセクションのルール \#3.1.2 が true である場合にのみルックアップが発生します。

**データ メソッド バインド**

1.  データ メソッドの戻り値が EDT である場合、「拡張データ型にバインドされたコントロール」セクションのルール \#1 と \# が適用されます。
2.  コントロールでルックアップまたは lookupReference が上書きされている場合。
    -   これには、registerOverrideMethod を使用した上書きも含まれます。

## <a name="multiselect-lookups"></a>複数選択のルックアップ
### <a name="available-system-forms-for-building-multi-select-lookups"></a>複数選択ルックアップを構築するために利用可能なシステム フォーム

現在、複数選択ルックアップを作成するためのシステム フォームが 2 つあります。

-   SysLookup: 列挙に基づいて複数選択します。
-   SysLookupMultiselectGrid: データの収集に基づいて複数選択します。

### <a name="what-happened-to-the-syslookupmultiselect-form"></a>SysLookupMultiselect フォームの変更点とは

SysLookupMultiselect は、Microsoft Dynamics AX 2012 で廃止の対象としてマークされ、削除されました。 複数選択のルックアップ シナリオでこのフォームを使用する場合、SysLookupMultiselectGrid を使用するように移行する必要があります。 例については、チュートリアル\_LookupMultiSelectGrid のフォームを参照してください。

## <a name="unsupported-lookup-scenarios"></a>検索シナリオはサポートされていません
### <a name="creating-multiple-lookup-forms-when-the-lookup-button-is-used"></a>ルックアップ ボタンが使用されているときの複数のルックアップ フォームを作成しています

ルックアップ ボタンを使用して複数のルックアップ フォームを作成する場合にエラーが発生する可能性があります。 たとえば、「ルックアップ」メソッドを上書きして新しいルックアップ フォームを作成しても、「スーパー」 (別のルックアップ フォームを作成します) も呼び出します。

### <a name="using-selectedcontrol-to-determine-which-control-is-hosting-a-lookup"></a>SelectedControl() を使用してルックアップをホストしているコントロールを決定

ルックアップをホストしているコントロールを決定する SelectedControl() の使用はサポートされていません。 場合によっては動作しますが、他の場合には失敗します。 たとえば、曖昧性解消ルックアップでは、コントロールを離れる行為は、曖昧性解消ルックアップをトリガーすることであるため、親フォーム上でコントロールは選択されていません。。 SelectedControl() を使用する代わりに、ルックアップをホストしているコントロールを取得するいくつかの方法があります。
-   ルックアップ フォームの「selectTarget」を確認してください。
    ```xpp
    FormStringControl selectTarget = formRun.selectTarget();
    ```

-   ルックアップ フォーム引数の「callerFormControl」を確認してください。 SysTableLookup::getCallerControl(Args args) はその呼び出しをカプセル化することに注意してください。
    ```xpp
    FormStringControl argsCallerFormControl = args.callerFormControl();
    ```
    
ルックアップ フォーム インスタンスがカーネルによって自動的にスピン アップされる場合、selectTarget および callerFormControl が自動的に設定されることに注意してください。 フォーム インスタンスがアプリケーション コードで作成される場合、これらを次のように手動で設定できます。

```xpp
public void lookup()
{
    Args args = new Args(formStr(<formName>));
    args.caller(element);
    args.callerFormControl(this);
    FormRun formRun = classfactory.formRunClass(args);
    formRun.init();
    this.performFormLookup(formRun);
}
```

### <a name="creating-a-slider-dialog-instead-of-a-lookup-form-when-the-lookup-button-is-used"></a>ルックアップ ボタンを使用する際のスライダーのダイアログ (ルックアップ フォームの代わりに) を作成しています

ルックアップ ボタンを使用すると、ルックアップ コントロールによってルックアップ フォームを開く必要があります (スライダー ダイアログまたはその他の種類のフォームではありません)。  これの第 1 の理由は、製品の整合性を保つことです。 2 番目の重要な理由は、ルックアップからスライダー ダイアログを開くことは、ルックアップの新しい先行入力機能と互換性がないことです。





[!INCLUDE[footer-include](../../../includes/footer-banner.md)]