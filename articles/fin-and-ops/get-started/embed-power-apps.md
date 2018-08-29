---
title: "PowerApps アプリの埋め込み"
description: "このトピックでは、PowerApps を Finance and Operations クライアントに組み込んで製品の機能を拡張する方法について説明します。"
author: jasongre
manager: AnnBe
ms.date: 06/08/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
ms.search.form: FormRunConfigurationAddPAControl, FormRunConfigurationEditPAControl
audience: Application User, Developer, IT Pro
ms.search.scope: Operations, Core
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2018-02-28
ms.dyn365.ops.version: Platform update 14
ms.translationtype: HT
ms.sourcegitcommit: 764d4c9049d94ebcd55c61654aa2f4133b35bae6
ms.openlocfilehash: 3b0bb61a52721f1e2eaf6df53e17b6cc162d8409
ms.contentlocale: ja-jp
ms.lasthandoff: 08/09/2018

---

# <a name="embed-powerapps-apps"></a>PowerApps アプリの埋め込み

[!include [banner](../includes/banner.md)]

プラットフォーム update 14 で、Microsoft Dynamics 365 for Finance and Operations は Microsoft PowerApps との統合をサポートし、コードの記述なしでモバイル デバイス、タブレット、および Web のカスタム ビジネス アプリを構築するため、開発者および技術者以外のユーザー向けのサービスをサポートします。 ユーザー、組織、またはより幅広いエコシステムによって開発された PowerApps を、Finance and Operations のクライアントに組み込み、製品の機能を拡張することができます。 たとえば、PowerApp を構築して、別のシステムから取得した情報で Finance and Operations を補足することができます。 

PowerApps の組み込みに関する詳細については、短い [PowerApps を Dynamics 365 for Finance and Operations に組み込む方法](https://www.youtube.com/watch?v=x3qyA1bH-NY) ビデオを確認してください。

## <a name="adding-an-embedded-powerapp-to-a-page"></a>埋め込まれた PowerApp をページに追加する。
### <a name="overview"></a>概要
Finance and Operations クライアントに PowerApp を埋め込む前に、最初に、必要なビジュアルまたは機能を備えた PowerApp を見つけたり構築したりする必要があります。 ここでは、PowerApp を構築するための詳細なプロセスについては説明しません。 [PowerApps の概要](https://docs.microsoft.com/en-us/powerapps/getting-started) トピックは、PowerApps を初めて使用する場合に有用です。

特定の PowerApp を組み込む準備ができたら、ページ上の PowerApp にアクセスする 2 つの方法のうち、いずれかシナリオに適したルートを選択できます。 最初の方法は、標準のアクション ペインに追加された PowerApps ボタンを使用することです。 このメカニズムを使用して追加された PowerApps は、PowerApps メニュー ボタンのメニュー項目として表示されます。 これらのメニュー項目を選択すると、埋め込まれた PowerApp を含む作業ウィンドウが開きます。 または、PowerApp を新しいタブ、クイック タブ、ブレード、またはワークスペースで新しいセクションとしてページに直接表示することもできます。 

組み込みの PowerApp を Finance and Operations で設定するときは、PowerApp への入力として送信する単一のフィールドを選択できます。 これにより、現在 Finance and Operations で表示しているデータに基づいて PowerApp を応答させることができます。  

### <a name="details"></a>細目
次の手順では、Finance and Operations Web クライアントに、PowerApp を組み込む方法を示しています。  

1. PowerApp を埋め込むページに移動します。 これは、入力として PowerApp に渡す必要があるデータを含む同じページになります。  
2. **PowerApp を挿入**ウィンドウを開きます。
   - **オプション**をクリックし、**このフォームのパーソナライズ**を選択します。 **挿入**メニューで、**PowerApp** を選択します。 最後に、PowerApp を追加する地域を選択します。 PowerApps メニュー ボタンの下で PowerApp を埋め込む場合、アクション ウィンドウを選択します。 ページに直接 PowerApp を埋め込む場合、適切なタブ、クイック タブ、ブレード、またはセクション (ワークスペースにいる場合) を選択します。   
   - PowerApps メニュー ボタンを使用して PowerApp にアクセスする場合、代わりに標準のアクション ウィンドウの **PowerApps** メニュー ボタンをクリックし、**PowerApp の挿入**を選択します。  
3. 埋め込み型 PowerApps を構成します。
   - **名前**フィールドは、埋め込まれた PowerApp を含むボタンまたはタブのテキストを示します。 多くの場合、このフィールドで PowerApp の名前を繰り返すことができます。  
   - **アプリ ID** は、埋め込む PowerApp の GUID です。 この値を取得するには、[web.powerapps.com](https://web.powerapps.com) で PowerApp を検索し、**詳細**の**アプリ ID** フィールドを探します。  
   - **PowerApp のデータを入力する**では、必要に応じて、 PowerApp に入力として渡すデータが含まれているフィールドを選択することができます。 PowerApp が Finance and Operations から送信されるデータにどのようにアクセスするかの詳細に関しては、このトピックの後の [Finance and Operations からのデータを活用する PowerApp の構築](#building-a-powerapp-that-leverages-data-sent-from-finance-and-operations) を参照してください。  
   - 埋め込む PowerApp のタイプに一致する**アプリケーション サイズ**を選択します。 モバイル デバイス用に作成された PowerApps に対しては**シン**を選択し、タブレット用に作成された PowerApps に対しては**ワイド**を選択します。 これにより、埋め込み PowerApp に十分な容量を確保できます。
   - **法人**クイック タブには、PowerApp が利用できる法人を選択する機能があります。 既定では、PowerApp はすべての法人で表示されます。  
4. コンフィギュレーションが正しいことを確認した後、**挿入**をクリックしてページに PowerApp を埋め込みます。 組み込みの PowerApp を表示するために、ブラウザを更新するよう求められます。 

## <a name="sharing-an-embedded-powerapp"></a>埋め込まれた PowerApp の共有
ページに PowerApp を埋め込み、ページから渡されたデータ コンテキストで正しく動作がしていることを確認したら、この埋め込まれた PowerApp をシステムで他のユーザーと共有することができます。 これは、製品の個人用設定機能を使用して、2つの異なる方法で実行できます。

- 推奨されるシナリオは、すべてのユーザーまたはユーザーのサブセットに個人用設定をプッシュできる、システム管理者によるものです。 

- または、ページの個人用設定をエクスポートし、1 つまたは複数のユーザーに送信し、これらの各ユーザーにその変更をインポートさせることもできます。 個人用設定のツールバー上の [管理] オプションで、個人用設定をエクスポートし、インポートすることができます。

製品での個人用設定の機能について、およびそれらの使用方法の詳細については、[ユーザー エクスペリエンスのパーソナライズ](personalize-user-experience.md) を参照してください。

## <a name="building-a-powerapp-that-leverages-data-sent-from-finance-and-operations"></a>Finance and Operations から送信されたデータを活用する PowerApp の構築
Finance and Operations に埋め込まれる PowerApp を構築するのに重要なのは、Finance and Operations からの入力データを使用することです。 PowerApp 内で、Param("EntityId") 変数を使用して入力データにアクセスできます。  

たとえば、PowerApp の OnStart 機能では、Finance and Operations から次のような変数に入力データを設定することができます。

If(!IsBlank(Param("EntityId")), Set(FinOpsInput, Param("EntityId")), Set(FinOpsInput, "")); 

## <a name="viewing-an-embedded-powerapp"></a>埋め込まれた PowerApp の表示
Finance and Operations のページに埋め込まれた PowerApp を表示するには、PowerApp が埋め込まれたページにそのまま移動します。 PowerApps は、標準アクション ペインの PowerApps ボタンからアクセスできます。また、新しいタブ、クイック タブ、ブレード、またはワークスペースの新しいセクションとしてページに直接表示することもできます。 ユーザーが最初に、ページ上に PowerApp を読み込もうとすると、PowerApps にサインインするように表示され、ユーザーにPowerApp を使用する適切なアクセス許可があることを確認します。   

## <a name="editing-an-embedded-powerapp"></a>埋め込まれた PowerApp の編集
PowerApp がページに埋め込まれた後、その PowerApp の設定をいくつか変更する必要がある場合があります。 たとえば、埋め込まれた PowerApp に関連付けられたラベルを変更したり、PowerApp の新しいバージョンが作成された場合に、最新の PowerApp を参照するようアプリ ID を更新したりする必要があります。 

埋め込まれた PowerApp のコンフィギュレーションを編集するには、次の手順に従います。
1. **PowerApp を編集**ウインドウに移動します。 
   - 埋め込み型の PowerApp が PowerApps メニュー ボタンによりアクセスされた場合、PowerApps メニュー ボタンを右クリックし、**パーソナライズ** を選択します。 **Select PowerApp** ドロップダウン メニューから構成する PowerApp を選択します。  
   - 埋め込み型の PowerApp がページに直接表示されたら、**オプション** を選択し、**このフォームのパーソナライズ** を選択します。 **選択** ツールを使用し、埋め込まれた PowerApp をクリックします。  
2. PowerApps コンフィギュレーションに必要な変更を行ない、**保存** をクリックします。  

## <a name="removing-an-embedded-powerapp"></a>埋め込まれた PowerApp の削除
PowerApp がページに埋め込まれた後、必要に応じて削除するには 2 つの方法があります。 

- このトピックの前半にある [埋め込み PowerApp を編集](#editing-an-embedded-powerapp) セクションからの手順を使用して、**PowerApp を編集**ウィンドウに移動します。 ウィンドウに、削除する埋め込み型 PowerApp の情報が表示されていることを確認してから、**削除**ボタンをクリックします。 

- 埋め込まれた PowerApp は、個人用設定データとして保存されるため、ページの個人用設定をクリアすると、そのページの埋め込まれた PowerApps も削除されます。 ページの個人用設定をクリアするのは、永久的なもので元に戻すことはできないことに注意してください。 ページの個人用設定を削除するには、**オプション**を選択し、**このフォームのパーソナライズ**をクリックします。 **管理**メニューで**クリア**ボタンを選択します。 ブラウザを更新した後、このページの以前のすべての個人用設定は、削除されます。 個人用設定を使用してページを最適化する方法の詳細については、[ユーザー エクスペリエンスの個人用設定](personalize-user-experience.md) を参照してください。  

## <a name="appendix"></a>付録 
### <a name="developer-control-over-where-a-powerapp-can-be-embedded"></a>PowerApp 埋め込み可能な場所についての開発者制御
既定では、ユーザーは、PowerApps メニュー ボタンの下または、タブ、クイック タブ、ブレード、またはワークスペースの新しいセクションとして任意のページに直接 PowerApps を埋め込むことができます。 ただし、必要に応じて開発者が次の方法を実装することで、PowerApps の埋め込みを特定のページのみに許可するようこの機能を構成することもできます。 

- **isPowerAppPersonalizationEnabled** - このメソッドが、特定のページに対して false を返す場合、PowerApps メニュー ボタンは表示されませんが、ユーザーは、タブを含む、このページのどこにも PowerApps を埋め込むことはできません。 

- **isPowerAppTabPersonalizationEnabled** - このメソッドが、特定のページに対して false を返す場合、タブ、クイック タブ、またはパノラマ セクションとしてページに直接 PowerApps を埋め込むことはできません。 ページで埋め込みが許可されている場合でも、ユーザーは PowerApps メニュー ボタンを使用して PowerApps を埋め込むことができます。  

次の例は、PowerApps を埋め込むための構成をするために必要な 2 つのメソッドを持つ新しいクラスを示しています。  

```
[ExtensionOf(classStr(FormRunConfigurationPowerAppsConfiguration))]

public final class ClassTest_Extension
{

    public static boolean isPowerAppPresonalizationEnabled(str pageName)
    {
        var result = next isPowerAppPresonalizationEnabled(pageName);
        return true;
    }

    public static boolean isPowerAppTabPresonalizationEnabled(str pageName)   
    {
        var result = next isPowerAppTabPresonalizationEnabled(pageName);
        return true;
    }
    ```

}


