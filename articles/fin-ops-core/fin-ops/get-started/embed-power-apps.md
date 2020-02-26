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
ms.openlocfilehash: 9585d5a399ebf45b0ad7640f3c4e48d8afc46cd8
ms.sourcegitcommit: 54baab2a04e5c534fc2d1fd67b67e23a152d4e57
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/04/2020
ms.locfileid: "3017731"
---
# <a name="embed-microsoft-power-apps"></a>埋め込み Microsoft Power Apps

[!include [banner](../includes/banner.md)]

Finance and Operations で、Microsoft Power Apps との統合をサポートし、コードの記述なしでモバイル デバイス、タブレット、および Web のカスタム ビジネス アプリを構築するため、開発者および技術者以外のユーザー向けのサービスをサポートします。 ユーザー、組織、またはより幅広いエコシステムによって開発された Power Apps を、Finance and Operations アプリに組み込み、製品の機能を拡張することができます。 たとえば、別のシステムから取得した情報を使用して Power Apps から Finance and Operations アプリを補足するアプリを構築する可能性があります。

Power Apps の埋め込みに関する詳細については、短い [Power Apps を組み込む方法](https://www.youtube.com/watch?v=x3qyA1bH-NY) ビデオを確認してください。

## <a name="adding-an-embedded-app-from-power-apps-to-a-page"></a>埋め込まれたアプリを Power Apps からページに追加する

### <a name="overview"></a>概要

Power Apps からクライアントにアプリを埋め込む前に、最初に、必要なビジュアルまたは機能を備えたアプリを見つけたり構築したりする必要があります。 ここでは、アプリを構築するための詳細なプロセスについては説明しません。 [Power Apps の概要](https://docs.microsoft.com/powerapps/getting-started) トピックは、Power Apps を初めて使用する場合に有用です。

特定のアプリを組み込む準備ができたら、ページ上のアプリにアクセスする 2 つの方法のうち、いずれかシナリオに適したルートを選択できます。 最初の方法は、標準のアクション ペインに追加された Power Apps ボタンを使用することです。 このメカニズムを使用して追加されたアプリは、Power Apps メニュー ボタンのメニュー項目として表示されます。 これらのメニュー項目を選択すると、埋め込まれたアプリを含む作業ウィンドウが開きます。 または、アプリを新しいタブ、クイック タブ、ブレード、またはワークスペースの新しいセクションとしてページに直接埋め込むこともできます。

組み込みのアプリを設定するときは、アプリへのコンテキストとして送信する単一のフィールドを選択できます。 これにより、現在表示しているデータに基づいてアプリを応答させることができます。

### <a name="details"></a>詳細情報

次の手順では、Power Apps から Web クライアントにアプリを埋め込む方法を示します。

1. アプリを埋め込むページに移動します。 これは、入力としてアプリに渡す必要があるデータを含む同じページになります。
2. **Power Apps からアプリを追加**ウィンドウを開きます。

    - **オプション**をクリックし、**このページのパーソナライズ**を選択します。 **挿入**メニューで、**Power Apps** を選択します。 最後に、アプリを追加する地域を選択します。 Power Apps メニュー ボタンの下でアプリを埋め込む場合、アクション ウィンドウを選択します。 ページに直接アプリを埋め込む場合、適切なタブ、クイック タブ、ブレード、またはセクション (ワークスペースにいる場合) を選択します。
    - Power Apps メニュー ボタンを使用してアプリにアクセスする場合、代わりに標準のアクション ウィンドウの **Power Apps** メニュー ボタンをクリックし、**アプリの追加**を選択します。

3. 埋め込み型アプリを構成します。

    - **名前**フィールドは、埋め込まれたアプリを含むボタンまたはタブのテキストを示します。 多くの場合、このフィールドでアプリの名前を繰り返すことができます。
    - **アプリ ID** は、埋め込むアプリの GUID です。 この値を取得するには、[web.powerapps.com](https://web.powerapps.com) でアプリを検索し、**詳細**の**アプリ ID** フィールドを探します。
    - **アプリのコンテキストを入力する**では、必要に応じて、アプリに入力として渡すデータが含まれているフィールドを選択することができます。 アプリが Finance and Operations アプリから送信されるデータにアクセスする方法の詳細に関しては、このトピックの後の [Finance and Operations アプリからのデータを活用するアプリの構築](#building-a-power-app-that-leverages-data-sent-from-finance-and-operations-apps) を参照してください。
    - 埋め込むアプリのタイプに一致する**アプリケーション サイズ**を選択します。 モバイル デバイス用に作成されたアプリに対しては**シン**を選択し、タブレット用に作成されたアプリに対しては**ワイド**を選択します。 これにより、埋め込みアプリに十分な容量を確保できます。
    - **法人**クイック タブには、アプリが利用できる法人を選択する機能があります。 既定では、アプリをすべての法人に対してアクセス可能にします。 このオプションは、[保存されたビュー](saved-views.md) が無効になっている場合にのみ使用可能です。 

4. 構成が正しいことを確認した後、**挿入**をクリックしてページに Power App を埋め込みます。 組み込みアプリを表示するために、ブラウザを更新するよう求められます。

## <a name="sharing-an-embedded-app"></a>埋め込まれたアプリの共有

ページにアプリを埋め込み、ページから渡されたデータ コンテキストで正しく動作していることを確認したら、システムで他のユーザーと共有することができます。 これは、製品の個人用設定機能を使用して、2つの異なる方法で実行できます。

- 推奨されるシナリオは、すべてのユーザーまたはユーザーのサブセットに個人用設定をプッシュできる、システム管理者によるものです。
- または、ページの個人用設定をエクスポートし、1 つまたは複数のユーザーに送信し、これらの各ユーザーにその変更をインポートさせることもできます。 個人用設定のツールバーには、個人用設定のエクスポートおよびインポートをするアクションがあります。

製品での個人用設定の機能について、およびそれらの使用方法の詳細については、[ユーザー エクスペリエンスのパーソナライズ](personalize-user-experience.md) を参照してください。

## <a name="building-an-app-that-leverages-data-sent-from-finance-and-operations-apps"></a>Finance and Operations アプリから送信されたデータを活用するアプリの構築

Finance and Operations アプリに埋め込まれる Power Apps からアプリをビルドする際の重要な部分は、そのアプリケーションからの入力データを使用することです。 Power Apps 開発経験から、Finance and Operations から渡された入力データには Param("EntityId") 変数を使用してアクセスできます。

たとえば、アプリの OnStart 機能では、Finance and Operations アプリから次のような変数に入力データを設定することができます。

```
If(!IsBlank(Param("EntityId")), Set(FinOpsInput, Param("EntityId")), Set(FinOpsInput, ""));
```

## <a name="viewing-an-app"></a>アプリの表示

Finance and Operations アプリのページに埋め込まれたアプリを表示するには、アプリが埋め込まれたページにそのまま移動します。 アプリは、標準アクション ウィンドウの Power Apps ボタンからアクセスでき、また新しいタブ、クイック タブ、ブレード、またはワークスペースの新しいセクションとしてページに直接表示することもできます。 ユーザーが最初に、ページ上にアプリを読み込もうとするとサインインするように表示され、ユーザーにアプリを使用する適切なアクセス許可があることを確認します。

## <a name="editing-an-embedded-app"></a>埋め込まれたアプリの編集

アプリがページに埋め込まれた後、そのアプリの設定をいくつか変更する必要がある場合があります。 たとえば、埋め込まれたアプリに関連付けられたラベルを変更したり、アプリの新しいバージョンが作成された場合に、アプリ ID を最新の時点のものに更新したりする必要があります。

埋め込まれたアプリのコンフィギュレーションを編集するには、次の手順に従います。

1. **アプリの編集**ウインドウに移動します。

    - 埋め込み型のアプリが Power Apps メニュー ボタンによりアクセスされた場合、Power Apps メニュー ボタンを右クリックし、**パーソナライズ**を選択します。 **アプリの選択**ドロップダウン メニューから構成するアプリを選択します。
    - 埋め込み型のアプリがページに直接表示されたら、**オプション**を選択し、**このページのパーソナライズ**を選択します。 **選択**ツールを使用し、埋め込まれたアプリをクリックします。

2. アプリ コンフィギュレーションに必要な変更を行ない、**保存**をクリックします。

## <a name="removing-an-app"></a>アプリの削除

アプリがページに埋め込まれた後、必要に応じて削除するには 2 つの方法があります。

- このトピックの前半にある [埋め込みアプリの編集](#editing-an-embedded-power-app) セクションからの手順を使用して、**アプリの編集**ウィンドウに移動します。 ウィンドウに、削除する埋め込み型アプリの情報が表示されていることを確認してから、**削除**ボタンをクリックします。
- 埋め込まれたアプリは、個人用設定データとして保存されるため、ページの個人用設定をクリアすると、そのページの埋め込まれたアプリも削除されます。 ページの個人用設定をクリアするのは、永久的なもので元に戻すことはできないことに注意してください。 ページの個人用設定を削除するには、**オプション**を選択して**このページのパーソナライズ**、最後に**クリア** ボタンをクリックします。 ブラウザを更新した後、このページの以前のすべての個人用設定は、削除されます。 個人用設定を使用してページを最適化する方法の詳細については、[ユーザー エクスペリエンスのパーソナライズ](personalize-user-experience.md)を参照してください。

## <a name="appendix"></a>付録

### <a name="developer-control-over-where-an-app-can-be-embedded"></a>アプリが埋め込み可能な場所についての開発者制御

既定では、ユーザーは、Power Apps メニュー ボタンの下または、タブ、クイック タブ、ブレード、またはワークスペースの新しいセクションとして任意のページに直接をアプリを埋め込むことができます。 ただし、必要に応じて開発者が次の方法を実装することで、アプリの埋め込みを特定のページのみに許可するようこの機能を構成することもできます。

- **isPowerAppPersonalizationEnabled** ー このメソッドが、特定のページに対して false を返す場合、Power Apps メニュー ボタンは表示されず、ユーザーは、タブを含むこのページのどこにもアプリを埋め込むことができません。
- **isPowerAppTabPersonalizationEnabled** ー このメソッドが、特定のページに対して false を返す場合、タブ、クイック タブ、またはパノラマ セクションとしてページに直接アプリを埋め込むことはできません。 ページで埋め込みが許可されている場合でも、ユーザーは Power Apps メニュー ボタンを使用してアプリを埋め込むことができます。

次の例は、アプリを埋め込むための構成をするために必要な 2 つのメソッドを持つ新しいクラスを示しています。

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
