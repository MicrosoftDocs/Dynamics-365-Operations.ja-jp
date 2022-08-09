---
title: コードの移行 - コンテキスト メニュー コード
description: この記事では、コンテキスト メニュー ( ショートカット メニュー) に必要なプログラミング モデルの詳細情報を提供します。
author: jasongre
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Developer
ms.reviewer: sericks
ms.custom: 16301
ms.assetid: 8f3b62f2-4de6-4ea3-b3e6-1101d0fe308e
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: eac67923137bac888ceb74ba1204ad6b617f700e
ms.sourcegitcommit: 873d66c03a51ecb7082e269f30f5f980ccd9307f
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/06/2022
ms.locfileid: "9124474"
---
# <a name="code-migration---context-menu-code"></a>コードの移行 - コンテキスト メニュー コード

[!include [banner](../includes/banner.md)]

プログラミング モデルには、コンテキスト メニュー (ショートカット メニュー) が必要です。 この記事では、Microsoft Dynamics AX 2012 から財務と運用へのコンテキスト メニュー コードを移行するプロセスの概要を説明します。 また、コンテキスト メニューのユーザー エクスペリエンス (UX) ガイドラインも含まれています。

Dynamics AX 2012 およびそれ以前のバージョンでは、開発者が **PopupMenu** クラスを使用して右クリック コンテキスト メニュー (ショートカット メニュー) を変更していました。 このクラスは、Web 上で利用できない Microsoft Windows アプリケーション プログラミング インターフェイス (API) に依存していました。 財務と運用では、同様の機能を提供する代わりに **ContextMenu** API が作成されました。 以前は、**context()** メソッドと **showContextMenu()** メソッドのオーバーライドは、特定のコントロールのコンテキスト メニューを変更するためのエントリ ポイントでした。 これらの上書きには通常、コンテキスト メニューにオプションを追加したり、ユーザーの選択を処理するためのコードが含まれていました。 ユーザーの選択を処理するコードは、待機モデルを使用していました。 これらの上書きが削除され、待機モデルが消去されるため、開発者は次の 2 つの上書きを作成する必要があります。**getContextMenuOptions()** によりコンテキスト メニューのオプションを追加し、**selectedMenuOption()** によりユーザーの選択を処理します。

## <a name="migrate-context-menu-code"></a>コンテキスト メニュー コードの移行 
**PopupMenu** API から **ContextMenu** API への移行は、3 つの主な段階に分けることができます。

### <a name="step-1-add-a-constant-for-each-menu-option-that-must-be-added"></a>手順 1 追加する必要のあるメニュー オプションごとの定数の追加

**PopupMenu** クラスの古い **insertItem()** メソッドは、追加されたメニュー オプションの識別子を返しました。 この識別子は、将来の参照のために変数に保存されました。 開発者はメニュー識別子を定義するため、各オプションの定数を定義してコードの可読性を高めることをお勧めします。

-   フォーム レベルでは、コンテキスト メニューに追加されている各メニュー オプションの定数を追加します。 値は各コンテキスト メニュー内で一意でなければなりません。 フォームまたはコントロールで別の変数と競合する場合、古い変数名を変更する必要があることに注意してください。

#### <a name="before"></a>以前

```xpp
public void context()
{
    ...
    int listCreateRoot = listMenu.insertItem("@SYS5480");
    ...
```

#### <a name="after"></a>変更後

```xpp
[Form]
public class MainAccount extends FormRun
{
    ...
    public const int listCreateRoot = 1;
    ...
```

### <a name="step-2-build-the-context-menu"></a>手順 2 コンテキスト メニューの構築

サブメニューとメニュー オプションのリストを構築し、コントロールのコンテキスト メニューに追加します。

1.  コントロールの **getContextMenuOptions()** メソッドの上書きを追加します。
2.  新しいコンテキスト メニューと、メニューに追加するオプションを保持するリストを作成します。
    -   ContextMenu メニュー = 新しい ContextMenu();
    -   List menuOptions = new List(Types::Class);

3.  一覧にメニュー オプションを追加:
    -   ContextMenuOption option = ContextMenuOption::Create(label,identifier);
    -   menuOptions.addEnd(option);

4.  メニューにオプションのリストを追加します。
    -   menu.ContextMenuOptions(menuOptions);

5.  **return** ステートメントを変更します。
    -   return menu.Serialize();

### <a name="step-3-process-the-user-selection-from-the-context-menu"></a>手順 3 コンテキスト メニューからのユーザーの選択を処理

1.  コントロールの **selectedMenuOption()** メソッドの上書きを追加します。
2.  オプション処理用の **switch()** ステートメントを、このオーバーライドに移動します。

## <a name="code-example"></a>コードの例
このセクションでは、Dynamics AX 2012 から財務と運用へのコンテキスト メニューの移行について説明します。 **MainAccount** フォームが例として使用されます。

### <a name="original-code"></a>オリジナル コピー

```xpp
public void context()
{       
    PopupMenu  listMenu        = new PopupMenu(element.hWnd());
    int        listCreateRoot  = listMenu.insertItem("@SYS5480");
    int        selectedMenu;
    selectedMenu = listMenu.draw();
    switch (selectedMenu)
    {
        case -1:
            break;
        case listCreateRoot:
            mainAccount_ds.create();
            break;
        default:
            break;
    }
}
```

### <a name="migrated-code"></a>移行されたコード

```xpp
// Define new form-level constant for each context menu option
public const int listCreateRoot = 1;
// Define new override on the control for building the context menu
public str getContextMenuOptions()
{
    str ret;
    ContextMenu menu = new ContextMenu(); 
    ContextMenuOption option = ContextMenuOption::Create("@SYS5480", listCreateRoot);
    List menuOptions = new List(Types::Class); 
    // Add label and ID of menu option
    menuOptions.addEnd(option); 
    menu.ContextMenuOptions(menuOptions);
    return menu.Serialize();
}
// Define new override on the control for processing the user selection
public void selectedMenuOption(int selectedOption)
{
    switch (selectedOption)
    {
        case -1:
            break;
        case listCreateRoot:
            mainAccount_ds.create();
            break;
        default:
            break;
    }
}
```

## <a name="ux-guidelines-for-context-menus"></a>コンテキスト メニューの UX ガイドライン
コンテキスト メニューを移行する際、次のガイドラインを考慮してください。

-   最も重要なコマンドは、メニューの先頭にある必要があります。
-   右クリックの対象となる要素の現在の状態に適用されないコマンドを削除します。
-   右クリックはショートカットです。 したがって、コンテキスト メニューのコマンドは、**常に** ページの他の場所で利用できる必要があります。
-   コンテキスト メニューのサブメニューを作成しないでください。 サブメニューは使いにくくタッチ対応ではありません。
-   メニュー項目の数を 5 に制限します。




[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
