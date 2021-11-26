---
title: 生産現場の実行インターフェイスのカスタマイズ
description: このトピックでは、現在のフォームを拡張する方法、または生産現場実行インターフェイス用の新しいフォームおよびボタンを作成する方法について説明します。
author: johanhoffmann
ms.date: 11/08/2021
ms.topic: article
ms.search.form: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2021-11-08
ms.dyn365.ops.version: 10.0.24
ms.openlocfilehash: 414fe5d6e16ad125bc2b9bb7ed427e5db5180ec9
ms.sourcegitcommit: bc9e75c38e192664cde226ed3a94df5a0b304369
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/10/2021
ms.locfileid: "7790980"
---
# <a name="customize-the-production-floor-execution-interface"></a>生産現場の実行インターフェイスのカスタマイズ

[!include [banner](../includes/banner.md)]

開発者は、現在のフォームを拡張したり、または生産現場実行インターフェイス用のフォームおよびボタンを独自に作成したりすることができます。 これらの新しい要素のコードを追加した後、管理者または生産現場マネージャーは、標準の構成制御を使用して簡単にインターフェイスに追加できます。

たとえば、メイン フォームで新しい列が必要な場合に考えられる解決策を次に示します。

- `JmgProductionFloorExecutionMainGrid` フォームを拡張し、目的のフィールドを追加します。
- 新しいフォームを作成し、それを新しいメイン ビュー (タブ) として追加します。

## <a name="add-a-new-button-action"></a>新しいボタンを追加する (アクション)

新しいボタンを追加する (アクション) には、次の手順に従って、カスタム アクションを実装するクラスを作成します。

1. `<ExtensionPrefix>_JmgProductionFloorExecution<ActionName>Action` という名前の新しいクラスを作成します。次のようになります:

    - `<ExtensionPrefix>` は、通常会社名を使用して、ソリューションを一意に識別します。
    - `<ActionName>` はクラス一意の ID です。 通常は、アクションの種類を示します。

1. 新しいクラスは、`JmgProductionFloorExecutionAction` クラスを拡張する必要があります。
1. 必要なすべての方法をオーバーライドします。

たとえば、次のクラスのコードを参照してください。

- `JmgProductionFloorExecutionBreakAction` – レコードが不要な単純なアクションのクラス。
- `JmgProductionFloorExecutionReportFeedbackAction` – より複雑な機能を提供するクラス。

終了すると、新しいボタン (アクション) が Microsoft Dynamics 365 Supply Chain Management の **デザイン タブ** ページに自動的に表示されます。 そこでは、あなた (または管理者または生産現場マネージャー) が、標準のボタンを追加するのと同様に、プライマリーまたはセカンダリー ツール バーに簡単に追加できます。 その方法については、[生産現場の実行インターフェースをデザインする](production-floor-execution-tabs.md)を参照してください。

## <a name="add-a-new-main-view"></a>新しいメイン ビューの追加

1. 必要な要素と機能を持つ新しいフォームを作成します。 このフォームは、拡張機能ではなく新しいフォームです。 フォームを `<ExtensionPrefix>_JmgProductionFloorExecution<FormName>` という名前にします。次のようになります:

    - `<ExtensionPrefix>` は、通常会社名を使用して、ソリューションを一意に識別します。
    - `<FormName>` はフォームの一意の ID です。

1. `<ExtensionPrefix>_JmgProductionFloorExecution<FormName>` という名前のメニュー項目を作成します。
1. 新しいメニュー項目をリストに追加して `getMainMenuItemsList` メソッドを拡張する `<ExtensionPrefix>_JmgProductionFloorExecution<FormName>_Extension` という名前の拡張機能を作成します。 次のコードは、例を示しています。

    ```xpp
    [ExtensionOf(classStr(JmgProductionFloorExecutionForm))]
    public final class <ExtensionPrefix>_JmgProductionFloorExecutionForm<FormName>_Extension{
        static public List getMainMenuItemsList()
        {
            List menuItemList = next getMainMenuItemsList();
            menuItemList.addEnd(menuItemDisplayStr(<ExtensionPrefix>_JmgProductionFloorExecutionForm<FormName>));
            return menuItemList;
        }
    ```

終了すると、新しいメイン ビューが Supply Chain Management の **デザイン タブ** の **メイン ビュー** コンボ ボックスに自動的に表示されます。 そこでは、あなた (または管理者または生産現場マネージャー) が、標準のメイン ビューを追加するのと同様に、新規または既存タブに簡単に追加できます。 その方法については、[生産現場の実行インターフェースをデザインする](production-floor-execution-tabs.md)を参照してください。

## <a name="add-a-details-view"></a>詳細ビューの追加

1. 必要な要素と機能を持つ新しいフォームを作成します。 このフォームは、拡張機能ではなく新しいフォームであることに注意してください。 フォームを `<ExtensionPrefix>_JmgProductionFloorExecution<FormName>Detail` という名前にします。次のようになります: 

    - `<ExtensionPrefix>` は、通常会社名を使用して、ソリューションを一意に識別します。
    - `<FormName>` はフォームの一意の ID です。

1. `<ExtensionPrefix>_JmgProductionFloorExecution<FormName>Detail` という名前のメニュー項目を作成します。
1. 新しいメニュー項目をリストに追加して `getDetailsMenuItemList` メソッドを拡張する `<ExtensionPrefix>_JmgProductionFloorExecution<FormName>_Extension` という名前の拡張子を作成します。

終了すると、新しい詳細ビューが Supply Chain Management の **デザイン タブ** の **詳細ビュー** コンボ ボックスに自動的に表示されます。 そこでは、あなた (または管理者または生産現場マネージャー) が、標準の詳細ビューを追加するのと同様に、新規または既存タブに簡単に追加できます。 その方法については、[生産現場の実行インターフェースをデザインする](production-floor-execution-tabs.md)を参照してください。

## <a name="add-a-numeric-keypad-to-a-form-or-dialog"></a>フォームまたはダイアログへ数値を追加する

次の例は、フォームに数値キーパッドを追加する例を示しています。

1. 各フォームに含まれる数値キーパッド コントローラーの数は、そのフォームの数値キーパッド数と等しくなる必要があります。

    ```xpp
    private JmgProductionFloorExecutionNumpadController   numpadController1;
    private JmgProductionFloorExecutionNumpadController   numpadController2;
    private JmgProductionFloorExecutionNumpadController   numpadController3;
    ```

1. 各数値キーパッド コントローラーのビヘイビアーを設定し、各数値キーパッド コントローラーを数値キーパッド フォーム パーツに接続します。

    ```xpp
    /// <summary>
    /// Initializes all numpad controllers, defines their behavior and connects them with numpad form parts.
    /// </summary>
    public void initializeNumpadController()
    {
        numpadController1 = new JmgProductionFloorExecutionNumpadController();
        numpadController1.getValueFromNumpadDelegate += eventhandler(this.setQuanityValueFromNumpad_1);
        QuantityNumpad1.getPartFormRun().setNumpadController(numpadController1);
    
        numpadController2 = new JmgProductionFloorExecutionNumpadController();
        numpadController2.parmNumpadEnabled(false);
        numpadController2.parmNumpadValue(333.56);
        numpadController2.getValueFromNumpadDelegate += eventhandler(this.setQuanityValueFromNumpad_2);
        QuantityNumpad2.getPartFormRun().setNumpadController(numpadController2);
    }
    ```

## <a name="use-a-numeric-keypad-as-a-pop-up-dialog"></a>数値キーパッドをポップアップ ダイアログとして使用する

次の例では、ポップアップ ダイアログ用に数値キーパッド コントローラーを設定する 1 つの方法を示します。

```xpp
private void setupNumpadController()
{
    numpadController = new JmgProductionFloorExecutionNumpadController();
    numpadController.parmShouldNumpadShowOkCancelButtons(true);
    numpadController.setNumpadValueToParentFormDelegate += eventhandler(this.setQtyValueFromNumpad);
}
```

次の例では、数値キーパッド ポップアップ ダイアログを呼び出す 1 つの方法を示します。

```xpp
Args args = new Args();
args.name(formstr(JmgProductionFloorExecutionNumpad));
args.menuItemName(menuItemDisplayStr(JmgProductionFloorExecutionNumpad));
args.caller(element);
Object formRun = classfactory.formRunClass(args);
formRun.init();
formRun.setNumpadController(numpadController);
numpadController.setValueToNumpad(333.56);
formRun.run();
```

## <a name="additional-resources"></a>追加リソース

- [生産現場の実行インターフェースのスタイル](production-floor-execution-styles.md)
- [生産現場の実行インターフェースをデザインする](production-floor-execution-tabs.md)
