---
title: Power Apps からキャンバス アプリを埋め込む
description: このトピックでは、Microsoft Power Apps のキャンバス アプリをクライアントに埋め込み、製品の機能を拡張する方法について説明します。
author: jasongre
manager: AnnBe
ms.date: 09/11/2020
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
ms.openlocfilehash: e57e4567a80aa9f9ba5ac434b0d71204460e164f
ms.sourcegitcommit: 71ec2f48185b8104ca52ff70df52263ce5f87f26
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/25/2020
ms.locfileid: "3893110"
---
# <a name="embed-canvas-apps-from-power-apps"></a>Power Apps からキャンバス アプリを埋め込む

[!include [banner](../includes/banner.md)]

Microsoft Power Apps は開発者と技術者以外のユーザーがコードを記述せずにモバイル デバイス、タブレット、および Web 用のカスタム ビジネス アプリを構築できるようにするサービスです。 Finance and Operations アプリは Power Apps との統合をサポートします。 ユーザー、組織、またはより幅広いエコシステムが開発するキャンバス アプリは、製品の機能を拡張するために Finance and Operations アプリに組み込むことができます。 たとえば、別のシステムから取得した情報で Finance and Operations アプリを補完するために、Power Apps からキャンバス アプリを構築できます。

Power Apps の埋め込みに関する詳細については、短い [Power Apps を組み込む方法](https://www.youtube.com/watch?v=x3qyA1bH-NY) ビデオを確認してください。

## <a name="adding-an-embedded-canvas-app-from-power-apps-to-a-page"></a>埋め込みキャンバス アプリを Power Apps からページに追加する

### <a name="overview"></a>概要

Power Apps からクライアントにキャンバス アプリを埋め込む前に、目的のビジュアルまたは機能を備えたアプリを見つけるか構築する必要があります。 このトピックには、アプリを構築するプロセスの詳細な説明は含まれていません。 初めて Power Apps を使用する場合は、[Power Apps ドキュメント](https://docs.microsoft.com/powerapps/) を参照してください。

アプリを埋め込む準備ができたときにページ上の特定のキャンバス アプリにアクセスするには、2 つの方法があります。 シナリオに適したアプローチを選択できます。 最初のアプローチでは、標準のアクション ペインに追加された **Power Apps** ボタンを使用します。 このアプローチを使用して追加したアプリは、**Power Apps** メニュー ボタン上に項目として表示されます。 これらの項目の 1 つを選択すると、埋め込みアプリを含むサイド ペインが表示されます。 または、アプリを新しいタブ、クイック タブ、あるいはブレードとして、またはワークスペースの新しいセクションとしてページに直接埋め込むこともできます。

埋め込みキャンバス アプリを構成するときに、アプリへのコンテキストとして送信する単一のフィールドを選択できます。 この手順により、現在表示しているデータに基づいてアプリが応答できるようになります。

> [!NOTE]
> 現在、このメカニズムを使用して、モデル化されたアプリを埋め込むことはできません。  

### <a name="details"></a>細目

次の手順では、Power Apps から Web クライアントにキャンバス アプリを埋め込む方法を示します。

1. キャンバス アプリを埋め込むページに移動します。 このページは、入力としてアプリに渡す必要があるデータを含むページになります。
2. **Power Apps からアプリを追加**ウィンドウを開きます。

    - **オプション**をクリックし、**このページのパーソナライズ**を選択します。 **挿入**メニューで、**Power Apps** を選択します。 最後に、アプリを追加する地域を選択します。 Power Apps メニュー ボタンの下でアプリを埋め込む場合、アクション ウィンドウを選択します。 ページに直接アプリを埋め込む場合、適切なタブ、クイック タブ、ブレード、またはセクション (ワークスペースにいる場合) を選択します。
    - Power Apps メニュー ボタンを使用してアプリにアクセスする場合、代わりに標準のアクション ウィンドウの **Power Apps** メニュー ボタンをクリックし、**アプリの追加**を選択します。

3. 埋め込み型アプリを構成します。

    - **名前**フィールドは、埋め込まれたアプリを含むボタンまたはタブのテキストを示します。 多くの場合、このフィールドでアプリの名前を繰り返すことができます。
    - **アプリ ID** フィールドは、埋め込むキャンバス アプリのグローバル一意識別子 (GUID) を示します。 この値を取得するには、[web.powerapps.com](https://web.powerapps.com) でアプリを検索し、**詳細** の **アプリ ID** フィールドを確認します。
    - **アプリのコンテキストを入力する**では、必要に応じて、アプリに入力として渡すデータが含まれているフィールドを選択することができます。 アプリが Finance and Operations アプリから送信されるデータにアクセスする方法の詳細に関しては、このトピックの後の [Finance and Operations アプリから送信されるデータを活用するアプリの構築](#building-a-canvas-app-that-uses-data-that-is-sent-from-finance-and-operations-apps) セクションを参照してください。
    - 埋め込むアプリのタイプに一致する**アプリケーション サイズ**を選択します。 モバイル デバイス用に作成されたアプリに対しては**シン**を選択し、タブレット用に作成されたアプリに対しては**ワイド**を選択します。 これにより、埋め込みアプリに十分な容量を確保できます。
    - **法人**クイック タブには、アプリが利用できる法人を選択する機能があります。 既定では、アプリをすべての法人に対してアクセス可能にします。 このオプションは、[保存されたビュー](saved-views.md) が無効になっている場合にのみ使用可能です。 

4. 構成が正しいことを確認した後、**挿入**をクリックしてページに Power App を埋め込みます。 組み込みアプリを表示するために、ブラウザを更新するよう求められます。

## <a name="sharing-an-embedded-app"></a>埋め込まれたアプリの共有

ページにキャンバス アプリを埋め込み、そのページから渡されたデータ コンテキストで正しく動作することを確認したら、システム内の他のユーザーとアプリを共有できます。 埋め込みキャンバス アプリを共有するには、次の手順を実行します。

1. 適切なユーザーと [キャンバス アプリを共有](https://docs.microsoft.com/powerapps/maker/canvas-apps/share-app) して、Power Apps でアプリにアクセスできるようにします。 

2. 対象とするユーザーが適切な個人用設定を持っていることを確認して、ユーザーがページを表示したときに埋め込みアプリが表示されるようにします。 次のアプローチのいずれかを使用できます:

    - 推奨: [保存されたビュー](saved-views.md) 機能を使用して、埋め込みアプリを含むビューを作成して公開します。 このアプローチを使用すると、公開されたビューの対象となるセキュリティ ロールを持つすべてのユーザーが Finance and Operations アプリでアプリを確認できるようになります。 
    - 保存されたビュー機能を有効にしていない場合は、システム管理者が、埋め込みアプリを含む個人用設定をすべてのユーザーまたは一部のユーザーにプッシュすることができます。 また、ページの個人用設定をエクスポートして、1 人または複数のユーザーに送信することもできます。 これらの各ユーザーは、個人用設定をインポートできます。 個人用設定のツールバーには、個人用設定をエクスポートおよびインポートするためのアクションがあります。 
    
> [!NOTE]
> キャンバス アプリが外部ユーザーと共有されている場合、これらのユーザーは、Finance and Operations アプリ内の埋め込みアプリを使用できません。 ただし、Power Apps 内でアプリに直接アクセスできます。 外部ユーザーには、Finance and Operations アプリが配置されている Microsoft 365 Azure ディレクトリに属さないゲストとユーザーが含まれます。

製品での個人用設定の機能について、およびそれらの使用方法の詳細については、[ユーザー エクスペリエンスのパーソナライズ](personalize-user-experience.md) を参照してください。

## <a name="building-a-canvas-app-that-uses-data-that-is-sent-from-finance-and-operations-apps"></a>Finance and Operations アプリから送信されるデータを使用するキャンバス アプリの構築

Finance and Operations アプリに埋め込まれるキャンバス アプリを構築する場合、プロセスの重要な部分の 1 つは、Finance and Operations アプリからの入力データを使用することです。 Power Apps 開発経験から、Finance and Operations アプリから渡される入力データには、**Param("EntityId")** 変数を使用してアクセスできます。

たとえば、アプリの OnStart 機能では、Finance and Operations アプリから次のような変数に入力データを設定することができます。

```powerapps
If(!IsBlank(Param("EntityId")), Set(FinOpsInput, Param("EntityId")), Set(FinOpsInput, ""));
```

## <a name="viewing-a-canvas-app"></a>キャンバス アプリの表示

Finance and Operations アプリのページに埋め込みキャンバス アプリを表示するには、埋め込みアプリがあるページに移動するだけです。 標準アクション ペインの **Power Apps** ボタンを使用してアプリにアクセスできることに注意してください。 または、新しいタブ、クイック タブ、あるいはブレードとして、またはワークスペースの新しいセクションとしてページに直接表示することもできます。 ユーザーがページに最初にアプリを読み込もうとすると、サインインするように求められます。 この手順により、ユーザーはアプリを使用するための適切なアクセス許可を持っていることを確認します。

## <a name="editing-an-embedded-app"></a>埋め込まれたアプリの編集

アプリがページに埋め込まれた後、そのアプリの設定をいくつか変更する必要がある場合があります。 たとえば、埋め込まれたアプリに関連付けられたラベルを変更したり、アプリの新しいバージョンが作成された場合に、アプリ ID を最新の時点のものに更新したりする必要があります。

埋め込まれたアプリのコンフィギュレーションを編集するには、次の手順に従います。

1. **アプリの編集**ウインドウに移動します。

    - 埋め込み型のアプリが Power Apps メニュー ボタンによりアクセスされた場合、Power Apps メニュー ボタンを右クリックし、**パーソナライズ**を選択します。 **アプリの選択**ドロップダウン メニューから構成するアプリを選択します。
    - 埋め込み型のアプリがページに直接表示されたら、**オプション**を選択し、**このページのパーソナライズ**を選択します。 **選択**ツールを使用し、埋め込まれたアプリをクリックします。

2. アプリ コンフィギュレーションに必要な変更を行ない、**保存**をクリックします。

## <a name="removing-an-app"></a>アプリの削除

アプリがページに埋め込まれた後、必要に応じて削除するには 2 つの方法があります。

- このトピックの前半にある [埋め込みアプリの編集](#editing-an-embedded-app) セクションからの手順を使用して、**アプリの編集**ウィンドウに移動します。 ウィンドウに、削除する埋め込み型アプリの情報が表示されていることを確認してから、**削除**ボタンをクリックします。
- 埋め込まれたアプリは、個人用設定データとして保存されるため、ページの個人用設定をクリアすると、そのページの埋め込まれたアプリも削除されます。 ページの個人用設定をクリアするのは、永久的なもので元に戻すことはできないことに注意してください。 ページの個人用設定を削除するには、**オプション**を選択して**このページのパーソナライズ**、最後に**クリア** ボタンをクリックします。 ブラウザを更新した後、このページの以前のすべての個人用設定は、削除されます。 個人用設定を使用してページを最適化する方法の詳細については、[ユーザー エクスペリエンスのパーソナライズ](personalize-user-experience.md)を参照してください。

## <a name="appendix"></a>付録

### <a name="developer-specifying-where-an-app-can-be-embedded"></a>[開発者] アプリの埋め込み先の指定

既定では、ユーザーは、Power Apps メニュー ボタンの下または、タブ、クイック タブ、ブレード、またはワークスペースの新しいセクションとして任意のページに直接をアプリを埋め込むことができます。 ただし、必要に応じて開発者が次の方法を実装することで、アプリの埋め込みを特定のページのみに許可するようこの機能を構成することもできます。

- **isPowerAppPersonalizationEnabled** ー このメソッドが、特定のページに対して false を返す場合、Power Apps メニュー ボタンは表示されず、ユーザーは、タブを含むこのページのどこにもアプリを埋め込むことができません。
- **isPowerAppTabPersonalizationEnabled** ー このメソッドが、特定のページに対して false を返す場合、タブ、クイック タブ、またはパノラマ セクションとしてページに直接アプリを埋め込むことはできません。 ページで埋め込みが許可されている場合でも、ユーザーは Power Apps メニュー ボタンを使用してアプリを埋め込むことができます。

次の例は、アプリを埋め込むための構成をするために必要な 2 つのメソッドを持つ新しいクラスを示しています。

```powerapps
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
