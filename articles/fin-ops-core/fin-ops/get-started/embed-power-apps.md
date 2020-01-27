---
title: 埋め込み Power Apps
description: このトピックでは、Power Apps をクライアントに組み込んで製品の機能を拡張する方法について説明します。
author: jasongre
manager: AnnBe
ms.date: 12/02/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: FormRunConfigurationAddPAControl, FormRunConfigurationEditPAControl
audience: Application User, Developer, IT Pro
ms.reviewer: sericks
ms.search.scope: Operations, Core
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2018-02-28
ms.dyn365.ops.version: Platform update 14
ms.openlocfilehash: 8b5e64cb9ba916f9cbd628703394318b4044867b
ms.sourcegitcommit: dc953c316c396c45ddd596e25c2b358e39a95d84
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 12/02/2019
ms.locfileid: "2870244"
---
# <a name="embed-microsoft-power-apps"></a>埋め込み Microsoft Power Apps

[!include [banner](../includes/banner.md)]

プラットフォーム更新 14 で、Microsoft Power Apps との統合をサポートし、コードの記述なしでモバイル デバイス、タブレット、および Web のカスタム ビジネス アプリを構築するため、開発者および技術者以外のユーザー向けのサービスをサポートします。 Power Appsユーザー、組織、またはより幅広いエコシステムによって開発された PowerApps を、Finance and Operations アプリに組み込み、製品の機能を拡張することができます。 たとえば、Power App を構築して、別のシステムから取得した情報で Finance and Operations アプリを補足することができます。

Power Apps の埋め込みに関する詳細については、短い [Power Apps を組み込む方法](https://www.youtube.com/watch?v=x3qyA1bH-NY) ビデオを確認してください。

## <a name="adding-an-embedded-power-app-to-a-page"></a>埋め込まれた Power App をページに追加する。

### <a name="overview"></a>概要

クライアントに Power App を埋め込む前に、最初に、必要なビジュアルまたは機能を備えた Power App を見つけたり構築したりする必要があります。 ここでは、Power App を構築するための詳細なプロセスについては説明しません。 [Power Apps の概要](https://docs.microsoft.com/powerapps/getting-started) トピックは、Power Apps を初めて使用する場合に有用です。

特定の Power App を組み込む準備ができたら、ページ上の Power App にアクセスする 2 つの方法のうち、いずれかシナリオに適したルートを選択できます。 最初の方法は、標準のアクション ペインに追加された Power Apps ボタンを使用することです。 このメカニズムを使用して追加された Power Apps は、Power Apps メニュー ボタンのメニュー項目として表示されます。 これらのメニュー項目を選択すると、埋め込まれた Power App を含む作業ウィンドウが開きます。 または、Power App を新しいタブ、クイック タブ、ブレード、またはワークスペースで新しいセクションとしてページに直接表示することもできます。

組み込みの Power App を設定するときは、Power App への入力として送信する単一のフィールドを選択できます。 これにより、現在表示しているデータに基づいて Power App を応答させることができます。

### <a name="details"></a>詳細情報

次の手順では、Web クライアントに Power App を埋め込む方法を示します。

1. Power App を埋め込むページに移動します。 これは、入力として Power App に渡す必要があるデータを含む同じページになります。
2. **Power App を挿入**ウィンドウを開きます。

    - **オプション**をクリックし、**このフォームのパーソナライズ**を選択します。 **挿入**メニューで、**Power App** を選択します。 最後に、Power App を追加する地域を選択します。 Power Apps メニュー ボタンの下で Power App を埋め込む場合、アクション ウィンドウを選択します。 ページに直接 Power App を埋め込む場合、適切なタブ、クイック タブ、ブレード、またはセクション (ワークスペースにいる場合) を選択します。
    - Power Apps メニュー ボタンを使用して Power App にアクセスする場合、代わりに標準のアクション ウィンドウの **Power Apps** メニュー ボタンをクリックし、**Power App の挿入**を選択します。

3. 埋め込み型 Power Apps を構成します。

    - **名前**フィールドは、埋め込まれた Power App を含むボタンまたはタブのテキストを示します。 多くの場合、このフィールドで Power App の名前を繰り返すことができます。
    - **アプリ ID** は、埋め込む Power App の GUID です。 この値を取得するには、[web.powerapps.com](https://web.powerapps.com) で Power App を検索し、**詳細**の**アプリ ID** フィールドを探します。
    - **Power App のデータを入力する**では、必要に応じて、 Power App に入力として渡すデータが含まれているフィールドを選択することができます。 Power App が Finance and Operations アプリから送信されるデータにどのようにアクセスするかの詳細に関しては、このトピックの後の [Finance and Operations アプリからのデータを活用する Power App の構築](#building-a-power-app-that-leverages-data-sent-from-finance-and-operations-apps)を参照してください。
    - 埋め込む Power App のタイプに一致する**アプリケーション サイズ**を選択します。 モバイル デバイス用に作成された Power Apps に対しては**シン**を選択し、タブレット用に作成された Power Apps に対しては**ワイド**を選択します。 これにより、埋め込み Power App に十分な容量を確保できます。
    - **法人**クイック タブには、Power App が利用できる法人を選択する機能があります。 既定では、Power App はすべての法人で表示されます。

4. 構成が正しいことを確認した後、**挿入**をクリックしてページに Power App を埋め込みます。 組み込みの Power App を表示するために、ブラウザを更新するよう求められます。

## <a name="sharing-an-embedded-power-app"></a>埋め込まれた Power App の共有

ページに Power App を埋め込み、ページから渡されたデータ コンテキストで正しく動作がしていることを確認したら、この埋め込まれた Power App をシステムで他のユーザーと共有することができます。 これは、製品の個人用設定機能を使用して、2つの異なる方法で実行できます。

- 推奨されるシナリオは、すべてのユーザーまたはユーザーのサブセットに個人用設定をプッシュできる、システム管理者によるものです。
- または、ページの個人用設定をエクスポートし、1 つまたは複数のユーザーに送信し、これらの各ユーザーにその変更をインポートさせることもできます。 個人用設定のツールバー上の [管理] オプションで、個人用設定をエクスポートし、インポートすることができます。

製品での個人用設定の機能について、およびそれらの使用方法の詳細については、[ユーザー エクスペリエンスのパーソナライズ](personalize-user-experience.md) を参照してください。

## <a name="building-a-power-app-that-leverages-data-sent-from-finance-and-operations-apps"></a>Finance and Operations アプリから送信されたデータを活用する Power App の構築

Finance and Operations アプリに埋め込まれる Power App を構築するのに重要なのは、Finance and Operations アプリからの入力データを使用することです。 Power App 内で、Param("EntityId") 変数を使用して入力データにアクセスできます。

たとえば、Power App の OnStart 機能では、Finance and Operations アプリから次のような変数に入力データを設定することができます。

```
If(!IsBlank(Param("EntityId")), Set(FinOpsInput, Param("EntityId")), Set(FinOpsInput, ""));
```

## <a name="viewing-an-embedded-power-app"></a>埋め込まれた Power App の表示

Finance and Operations アプリのページに埋め込まれた Power App を表示するには、Power App が埋め込まれたページにそのまま移動します。 Power Apps は、標準アクション ペインの Power Apps ボタンからアクセスできます。また、新しいタブ、クイック タブ、ブレード、またはワークスペースの新しいセクションとしてページに直接表示することもできます。 ユーザーが最初に、ページ上に Power App を読み込もうとすると、Power Apps にサインインするように表示され、ユーザーに Power App を使用する適切なアクセス許可があることを確認します。

## <a name="editing-an-embedded-power-app"></a>埋め込まれた Power App の編集

Power App がページに埋め込まれた後、その Power App の設定をいくつか変更する必要がある場合があります。 たとえば、埋め込まれた Power App に関連付けられたラベルを変更したり、Power App の新しいバージョンが作成された場合に、最新の Power App を参照するようアプリ ID を更新したりする必要があります。

埋め込まれた Power App のコンフィギュレーションを編集するには、次の手順に従います。

1. **Power App を編集**ウインドウに移動します。

    - 埋め込み型の Power App が Power Apps メニュー ボタンによりアクセスされた場合、Power Apps メニュー ボタンを右クリックし、**パーソナライズ**を選択します。 **Select Power App** ドロップダウン メニューから構成する Power App を選択します。
    - 埋め込み型の Power App がページに直接表示されたら、**オプション**を選択し、**このフォームのパーソナライズ**を選択します。 **選択**ツールを使用し、埋め込まれた Power App をクリックします。

2. Power Apps コンフィギュレーションに必要な変更を行ない、**保存**をクリックします。

## <a name="removing-an-embedded-power-app"></a>埋め込まれた Power App の削除

Power App がページに埋め込まれた後、必要に応じて削除するには 2 つの方法があります。

- このトピックの前半にある[埋め込み Power App を編集](#editing-an-embedded-power-app)セクションからの手順を使用して、**Power App を編集**ウィンドウに移動します。 ウィンドウに、削除する埋め込み型 Power App の情報が表示されていることを確認してから、**削除**ボタンをクリックします。
- 埋め込まれた Power App は、個人用設定データとして保存されるため、ページの個人用設定をクリアすると、そのページの埋め込まれた Power Apps も削除されます。 ページの個人用設定をクリアするのは、永久的なもので元に戻すことはできないことに注意してください。 ページの個人用設定を削除するには、**オプション**を選択し、**このフォームのパーソナライズ**をクリックします。 **管理**メニューで**クリア**ボタンを選択します。 ブラウザを更新した後、このページの以前のすべての個人用設定は、削除されます。 個人用設定を使用してページを最適化する方法の詳細については、[ユーザー エクスペリエンスのパーソナライズ](personalize-user-experience.md)を参照してください。

## <a name="appendix"></a>付録

### <a name="developer-control-over-where-a-power-app-can-be-embedded"></a>Power App 埋め込み可能な場所についての開発者制御

既定では、ユーザーは、Power Apps メニュー ボタンの下または、タブ、クイック タブ、ブレード、またはワークスペースの新しいセクションとして任意のページに直接 Power Apps を埋め込むことができます。 ただし、必要に応じて開発者が次の方法を実装することで、Power Apps の埋め込みを特定のページのみに許可するようこの機能を構成することもできます。

- **isPowerAppPersonalizationEnabled** ー このメソッドが、特定のページに対して false を返す場合、Power Apps メニュー ボタンは表示されず、ユーザーは、タブを含むこのページのどこにも Power Apps を埋め込むことができません。
- **isPowerAppTabPersonalizationEnabled** ー このメソッドが、特定のページに対して false を返す場合、タブ、クイック タブ、またはパノラマ セクションとしてページに直接 Power Apps を埋め込むことはできません。 ページで埋め込みが許可されている場合でも、ユーザーは Power Apps メニュー ボタンを使用して Power Apps を埋め込むことができます。

次の例は、Power Apps を埋め込むための構成をするために必要な 2 つのメソッドを持つ新しいクラスを示しています。

```
[ExtensionOf(classStr(FormRunConfigurationPowerAppsConfiguration))]

public final class ClassTest_Extension
{
    public static boolean isPowerAppPersonalizationEnabled(str pageName)
    {
        var result = next isPowerAppPersonalizationEnabled(pageName);
        return result;
    }
    
    public static boolean isPowerAppTabPersonalizationEnabled(str pageName)
    {
        var result = next isPowerAppTabPersonalizationEnabled(pageName);
        return result;
    }
}
```
