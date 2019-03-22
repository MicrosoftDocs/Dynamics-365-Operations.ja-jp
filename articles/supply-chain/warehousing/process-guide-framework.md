---
title: プロセス ガイド フレームワーク
description: このトピックでは、X++ で倉庫モバイル プロセスを拡張する開発者のプロセス ガイド フレームワークに関する情報を提供します。
author: MarkusFogelberg
manager: AnnBe
ms.date: 11/01/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Developer
ms.reviewer: shylaw
ms.search.scope: Operations
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: mafoge
ms.search.validFrom: 2018-4-30
ms.dyn365.ops.version: 8
ms.openlocfilehash: e3ee668aa5608790ee8d525aaf5faceeab65b6bd
ms.sourcegitcommit: 383a344deb5abf48584ea2ee7774b8dbbbec49b3
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/08/2019
ms.locfileid: "377894"
---
# <a name="process-guide-framework"></a>プロセス ガイド フレームワーク

[!include [banner](../includes/banner.md)]

このトピックでは、X++ で倉庫モバイル プロセスを拡張する開発者のプロセス ガイド フレームワークに関する情報を提供します。 倉庫モバイル プロセスは、小さなステップに分割されるプロセスの結果として拡張可能です。 各ステップのビジネス ロジックおよびユーザー インターフェイスの作成は、個々のクラスに抽出されたため、拡張可能になりました。

## <a name="overview-of-the-existing-design"></a>既存のデザインの概要

倉庫モバイル実行フローは、1 つのカスタム サービス エンドポイントを通じて公開されます。 ユーザーが入力した値に加えて、モバイル アプリケーションで表示されるユーザー インターフェイスのメタデータが含まれている、XML 文字列の形式でモバイル アプリケーションから要求が到達します。

要求が受信されると、この XML を逆シリアル化するために最初の手順が実行されます。 **WHSMobileAppServiceXMLTranslator** クラスは、コントロール情報とセッション情報の両方が含まれているコンテナーに XML を変換します。

その後、コンテナーの情報は、ユーザーが作業する倉庫プロセス、開始しようとしている倉庫プロセス (**WHSWorkExecuteMode** 列挙によって表される)、それに応じて **WHSWorkExecuteDisplay** の派生クラスをインスタンス化する倉庫プロセスを推定するために使用されます。 **displayform()** メソッドが呼び出された後、以下が実行されます。

-   ユーザーからのデータの処理 (**WHSRFControlData** クラスに委任されますが、いくつかのプロセスは、**processControl()** メソッドを上書きすることによって特定のロジックを実装します)。

-   ビジネス ロジックを実行します。

-   ステップが増加します。

-   新しいユーザー インターフェイスを表すコンテナーを構築します (一般に、**build…()** メソッドで)。

コンテナーは、その後、変換元に返却されて XML がシリアル化され、モバイル デバイスへの応答として返送されます。

次の順序図では、実行フローの概要を示します。 図は概要図以上のものでり、実際のコードを 1:1 で表したものではないことに注意してください。

![プロセスの概要図](media/schematic-overview.png)  

### <a name="reason-for-the-redesign"></a>再設計の理由

上記の設計には、モバイル フローで使用されるプロセスを作成するための非常に単純なフレームワークが用意されています。 ただし、上記で明らかなように、**displayform()** メソッドが複数の職責を引き継ぎます。 その他のメソッドおよびクラスに委任されますが、具体的なクラス職責がない場合は、クラス間で一貫性のある方法で実行されません。 また、サポートされるシナリオの数が増えるにつれて、これらのクラスの一部には非常に複雑になります。 問題をより魅力的にするために、これらのクラス/メソッドの一部が上書きされ、複数のモードで再利用されます。 結果は、サイクロマティック複雑度の高い非常に長いメソッドです。 過去には、保守の問題が生じていました。 これらのメソッドのバグを修正することは危険であり、後戻りする傾向がありました。
たとえば、**WhsWorkExecuteDisplay** クラス内の **processWorkLine()** メソッドは、複数のプロセス (基本的に、作業の実行が実行される任意の場所) から参照されます。

これらを拡張可能にするため、いずれかのオプションは、**displayForm** メソッドを小さなメソッドに分割して拡張ポイントを導入するためのものです。 ただし、シナリオ マトリックスのため、拡張機能を記述し、逆光を検証することはパートナーにとって困難です。 それだけでなく、上記の構造化された責任の配分がないため、コードは徐々に予期しない方法で増加し、品質の高い拡張機能を構築することが困難になります。

その結果、再設計は、明確に定義されたクラスに独立した職責を持たせるという目標を持つ、持続可能なオプションです。 クラスの職責、変更する理由、拡張する理由は 1 つにする必要があります。

## <a name="design-overview"></a>設計の概要

再設計されたフレームワークでは、中核的な戦略は 2 つの原則を中心に展開しています。実行フローを明確に定義された責任を持つ個々のコンポーネントに分割することと、各コンポーネントに適切に定義された拡張点を持つことです。

新しいフレームワークの名前は、"ProcessGuide" です。 これは、これらのクラスの目的が、業務プロセスを通じてユーザーをガイドすることだからです (データとやり取りする方法、またはタスクを実行する順序に関してユーザーがさらに柔軟性を持っているフォーム ベースのエクスペリエンスであるリッチ クライアントとは対照的)。

> [!NOTE]
> 1 つの重要な詳細は、"WHS" 接頭語の意図的な省略です。 モバイル プロセスは当初倉庫管理に導入されましたが、その結果、さまざまな生産および在庫管理プロセスをサポートするための超越した境界が生じました。 その結果、倉庫の参照はフレームワークの名前から除外されました。

コンポーネントを識別するために、まず、プロセスの生産の開始を調べます (**WhsWorkExecuteDisplayProdStart** クラス)。 次にプロセスの概要図を示します。

![プロセスの概要図の画像](media/production-start-process-schematic.png)

制御フローを見ると、次のコンポーネントが必要です。

-   ビジネス プロセス全体を通じて合成するコントローラー。
-   プロセスでステップの実行を担当するステップ。
-   ステップ内のデータを処理するためのデータ プロセッサ。
-   ステップのユーザー インターフェイスの作成を担当するページ ビルダー。
-   ステップの移行を担当するナビゲーション エージェント。
-   業務プロセスの実行を担当するクラス。

上のプロセス フロー図では、手順 1 から開始し、前の手順からのデータの処理を開始した後、最後に UI を構築した場合、データは次の手順で処理され続けます。 これにより、連続したステップ間に厳密な結合が生まれ、その結果、高レベルの新しい概略図は次のようになります。

![高レベルのプロセス概略図の画像](media/high-level-schematic.png)

以下は、再設計されたプロセスの重要なコンポーネントです。

-   **ProcessGuideController** - このクラスは、業務プロセスの全体的な実行を調整します。 これは、ステップとナビゲーション エージェントのインスタンスを作成し、その結果、プロセスの実行と、キャンセルまたはプロセスの終了のためのクリーンアップ ロジックを構成するファクトリを定義します。

-   **ProcessGuideStep** - このクラスは、業務プロセスの 1 つのステップを表します。 このクラスは、ページ ビルダー、アクション、およびデータ プロセッサのインスタンスを作成するファクトリの定義を含み、それらを正しい順序で呼び出することを担当します。

-   **ProcessGuideNavigationAgent** - このクラスは、手順間の移動を担当します。 ステップが完了したら、ナビゲーション エージェントは、次のステップの定義を担当し、前の手順が次の手順に伝達する必要があるすべてのパラメーターを渡します。

-   **ProcessGuidePageBuilder** - このクラスは、ユーザー インターフェイスのインスタンス化を担当します。

-   **ProcessGuideAction** - このクラスは、ユーザーにボタンとして表示される、アクションを表します。

-   **ProcessGuideDataProcessor** - このクラスは、フィールド内のユーザーが入力したデータの処理を担当します。

## <a name="execution-flow"></a>実行フロー

実行フローの開始点は変更されないままです。 そのため、要求は引き続き同じエンドポイントに到着し、その後、コンテナーに XML が逆シリアル化されます。 このコンテナーは、**getNextFormState()** にに渡されます。

注目すべき次の 3 つの重要なクラスがあります。

-  **ProcessGuideSessionState** - これは、セッション状態情報 (モード、合格、コントローラー、および実行される手順など) を含みます。

-  **ProcessGuidePage** - これには、ユーザー インターフェイス メタデータの厳密に表したものが含まれます。

-  **ProcessGuideRequest** - これには、メンバーとして上記の 2 つが含まれており、モバイル デバイスから受信した要求を厳密に表したものです。

これらのクラスは、コンテナー情報を使用して作成されます (状態とユーザー入力管理データの両方)。 これにより、値にアクセスして操作するためのタイプ セーフな方法が提供されます。 プロセス中のコンテナーの繰り返しアクセスと比較して、これは、信頼性とパフォーマンスの両方に関して利点を生み出します。

セッション状態情報は、適切な **ProcessGuideController** クラスのインスタンスを作成するために使用されます。 インスタンスが作成されると、**ProcessGuideController** クラス内の **createResponse()** メソッドが呼び出されます。 このメソッドは、プロセス ガイド ロジックへのエントリ ポイントであり、実行後、応答で戻ります (**ProcessGuideResponse** クラスで表される)。 応答は、その後コンテナーに変換されて、レガシ トピックに戻された後、XML にシリアル化され、応答がモバイル デバイスに戻されます。

次に、コントローラーは実行する次の手順を見つける必要があります。 これが新しいプロセスの開始である場合、コントローラーは **initialStep()** を呼び出して、プロセスの最初の手順を取得します。 その後、**ProcessGuideStep** で **execute()** メソッドを呼び出します。 この方法はその後、**ProcessGuidePageBuilder** クラスのインスタンスを作成し、**buildPage()** を呼び出します。これにより、ユーザーに表示されるユーザー インターフェイスの仮想表現である **ProcessGuidePage** オブジェクトが返されます。 その後、ステップは結果をコントローラーに戻します。それから、現在のセッションの状態が保存され、結果が **ProcessGuideResponse** クラスの形式で **getNextFormState()** に戻されます。 その後、応答はコンテナーにもう一度変換され、その結果、XML にシリアル化されて、モバイル デバイスに応答が返されます。

次のシーケンス図では、この制御フローについて説明します。 これは、設計を説明するために簡略化された、最も一般的な制御フローである点に注意してください。

![簡略化された制御フロー](media/control-flow.png)

ユーザーがボタンをクリックして (または、通常は既定のアクションをトリガーする値をスキャンして) モバイル デバイスでアクションを実行すると、要求は同じルートを経由して **ProcessGuideController** クラス内の **createResponse()** メソッドに到着します。 ただし、このとき、コントローラーはセッション状態情報から、ユーザーがいるステップを知ります。 したがって、適切な **ProcessGuideStep** クラスのインスタンスを作成し、実行メソッドを呼び出します。 同様に、**ProcessGuideStep**はユーザーによって呼び出されるアクション名を読み取り、適切な **ProcessGuideAction** クラスをインスタンス化して **execute()** を呼び出します。

**ProcessGuideAction** クラスは、特定のアクションを実行することを担当しますが、2 つの重要な例外があります。

1 つ目は、**ProcessGuideOKAction** クラスです。 このアクションは、ユーザーがプロセスを確認して前に動かすことを求めていることを意味します。 それに従って、このメソッドは実際に ProcessGuideStep クラスへのコールバックを行います。これは、ステップが **ProcessGuideDataProcessor** で **processData()** を呼び出すことを意味します。 これは、ユーザーが入力したデータを処理し、ステップの状態を更新し、結果をコントローラーに返します。 プロセッサの結果によっては、ステップは適切なユーザー インターフェイスを構築するためのページ ビルダーを起動するか、ステップのステータスを完了に設定します。 これは、次のシーケンス図の上半分に反映されています。

その他の例外は、**ProcessGuideCancelResetProcessAction** および **ProcessGuideCancelExitProcessAction** クラスで実装されている取消アクションです。 これらのアクションは、処理をキャンセルする意図を表し、プロセスの開始またはプロセスの終了を完全に戻します。 **OK** アクションと同様、これらのアクションも、ステップにコールバックを実行します。これは、**ProcessGuideController** に意図を示します。 その後、コントローラーは状態変数の必要なクリーンアップを実行し、コントロールをプロセスにおける最初のステップに移動するか、プロセスを完全に終了します。

ステップが完了した後、ステップのステータスが **完了** に設定されている場合、コントローラーは **ProcessGuideNavigationAgent** のインスタンスを作成し、次のステップの名前が返されます。 その後、コントローラーはこのステップをインスタンス化し、**execute()** メソッドを呼び出します。サイクルが続行します。 ほとんどの場合、新しい手順は、対応する **ProcessGuidePageBuilder** を呼び出し、ユーザーに表示した後に戻される次の画面のユーザー インターフェイスを作成します。 このフローは、次のシーケンス図の下半分に反映されています。

![シーケンス図](media/sequence-diagram.png)

## <a name="building-a-new-process-using-the-processguide-framework"></a>ProcessGuide フレームワークを使用した新しいプロセスの構築

制御フローを説明する最善の方法は、アプリケーションに存在している例を使用することです (生産開始プロセス)。

## <a name="overview-of-the-production-start-process"></a>生産開始プロセスの概要

まず、プロセス フローを理解しましょう。 最初の手順で、ユーザーは製造オーダー ID の入力を求められます。

![生産 ID の確認](media/production-id-prompt.png)

製造オーダー ID をユーザーが入力すると、注文番号が検証されます。 実行される検証の一部は、ユーザーがログインしているのと同じ倉庫に注文があるかどうかと、注文のステータスに基づいています。 検証が失敗すると、ユーザーにはエラー メッセージが表示されます。 検証が正常に実行された場合、ユーザーには、製造オーダーと品目の詳細が表示されます。

ユーザーはキャンセルしてプロセスの開始に戻るか、**OK** をクリックして確認できます。 後者の場合は、製造オーダーが **開始済** ステータスに設定され、対応する仕訳帳が転記され、コントロールが最初の手順に戻り、ユーザーに ”作業完了" というメッセージが表示されます。


## <a name="creating-the-controller"></a>コントローラーの作成

業務プロセスの作成の最初の手順は、コントローラー クラスの作成です。これは、コントローラーのデフォルトの動作を実装する **ProcessGuideController** 抽象クラスから拡張されます。 新しいクラスの名前は **ProdProcessGuideProductionStartController** であり、**StartProdOrder** の **WHSWorkExecuteMode** で修飾されます。 **WHSWorkExecuteDisplay** クラスで使用されたのと同じ **SysExtension** ベースのインスタンス化が使用されます。これは、ユーザーがこのモードのメニュー項目を実行するときにコントローラーをインスタンス化するのに役立ちます。

<pre><code>
[WHSWorkExecuteMode(WHSWorkExecuteMode::StartProdOrder)]
public class ProdProcessGuideProductionStartController extends ProcessGuideController</code></pre>

> [!NOTE]
> クラスの名前付けパターンは、**\<FunctionalArea\>ProcessGuide\<Businessprocessname\>Controller** です。 これは、コントローラー クラスに使用されるパターンであり、その他のクラスを拡張するためのものです。


## <a name="building-the-first-step"></a>最初のステップの作成

次に、最初のステップを定義するには、**ProcessGuideStep** から拡張して、**ProdProcessGuidePromptProductionIdStep** クラスを作成します。

クラスのインスタンス化を作成するタスクは、**ProcessGuideController** 基本クラスによって呼び出されるステップ ファクトリに委任されます。。 ファクトリの既定の実装は、名前に基づいてステップをインスタンス化します。 したがって、コントローラーの最初のステップとして **ProdProcessGuidePromptProductionIdStep** のインスタンスを作成するには、2 つの操作を行う必要があります。

-   **ProdProcessGuidePromptProductionIdStep** クラスを **ProcessGuideStepName** 属性で修飾します。

    ``[ProcessGuideStepName(classStr(ProdProcessGuidePromptProductionIdStep))] public class ProdProcessGuidePromptProductionIdStep extends ProcessGuideStep``

-   コントローラー クラスで、抽象メソッド **initialStepName()** を実装して、ステップの名前を戻します。

    ``protected final ProcessGuideStepName initialStepName()
    {
        return classStr(ProdProcessGuidePromptProductionIdStep);
     }``   
    
> [!NOTE]
> **ProcessGuideStepName** 属性の値は、上記のように、クラス名と完全に一致する必要はありません。 ただし、これを実装することにより、クラスを使用する場合の相互参照に関する均一性とタイプ セーフが生じます。 この名前付け規則を使用することをお勧めします。
>
> ステップの **ProcessGuideStepName** ベースのインスタンス化は、**ProcessGuideStepDefaultFactory** クラスで実装されます。 まれに、異なる戦略でステップのインスタンス化が必要になることがありますが、その場合は次のようにする必要があります。
> -   **ProcessGuidStepAbstractFactory** から継承する新しいファクトリ クラスを作成します。
> -   必要に応じて、ファクトリが必要とするパラメーターを含む **ProcessGuideIStepCreationParameters** インターフェイスを実装する新しいパラメーター クラスを作成します。
> -   コントローラー クラスで、**stepFactory()** および **stepCreationParameters()** メソッドを上書きし、上記のファクトリとパラメータを返します。

次のステップでは、**ProdProcessGuidePromptProductionIdStep** クラスの機能を実装します。 ユーザーが入力したデータを処理し、ステップがいつ完了するかを決定するためのユーザー インターフェイスを構築するためのロジックを実装する必要があります。

### <a name="building-the-user-interface-for-the-first-step"></a>最初のステップのユーザー インターフェイスの構築

ユーザー インターフェイスは、**ProcessGuidePageBuilder** 抽象クラスからから継承するクラスを使用して作成されます。 この手順では、**ProdProcessGuidePromptProductionIdPageBuilder** が何をするかを表すクラスを指定します。

クラスのインスタンス化メカニズムは、ステップがコントローラーからインスタンス化された方法と似ています。 

-   **ProdProcessGuidePromptProductionIdPageBuilder** クラスを **ProcessGuidePageBuilderName** 属性で修飾します。

``[ProcessGuidePageBuilderName(classStr(ProdProcessGuidePromptProductionIdPageBuilder))] public class ProdProcessGuidePromptProductionIdPageBuilder extends ProcessGuidePageBuilder``

-   **ProdProcessGuidePromptProductionIdStep** クラスで、抽象メソッド **pageBuilderName()** を実装してこの名前を返します。

    ``protected final ProcessGuidePageBuilderName pageBuilderName()
    {
        return classStr(ProdProcessGuidePromptProductionIdPageBuilder);
     }``    

> [!TIP]
> ステップ ファクトリと同様、ページ ビルダ ファクトリに実装される抽象ファクトリ パターンもあります。 ですから、まれに、異なる戦略でページ ビルダーのインスタンス化が必要になることがありますが、その場合は次のようにすることができます。
> - **ProcessGuidePageBuilderAbstractFactory** から継承する新しいファクトリ クラスを作成します。
> - 必要に応じて、ファクトリが必要とするパラメーターを含む **ProcessGuideIPageBuilderCreationParameters** インターフェイスを実装する新しいパラメーター クラスを作成します。
> - ステップ クラスで、**pageBuilderFactory()** および **pageBuilderCreationParameters()** メソッドを上書きし、上記のファクトリとパラメータを返します。

ユーザー インターフェイスを実装するには、製造オーダー ID を入力するための 1 つのテキスト ボックスに加えて、**OK** ボタンおよび **キャンセル** ボタンがあるページが必要です。 **キャンセル** ボタンは、プロセスを終了する必要があります。

これを実装するには、**ProdProcessGuidePromptProductionIdPageBuilder** クラスで 2 つのメソッドを上書きする必要があります。

-   **addDataControls()** メソッドを使用してテキスト ボックスを追加します。

    ``protected final void addDataControls(ProcessGuidePage _page)
    {
        _page.addTextBox(ProcessGuideDataTypeNames::ProdId, "@SYS4398", extendedTypeNum(ProdId));
     }``   

-   **addActionControls()** メソッドを使用して **OK** および **Cancel** ボタンを追加します。

    ``protected final void addActionControls(ProcessGuidePage _page) {
        #ProcessGuideActionNames
        _page.addButton(step.createAction(#ActionOK), true);
        _page.addButton(step.createAction(#ActionCancelExitProcess));
     }``   

これは、ボタンの前に、データ コントロールを追加します。 ただし、データ コントロールとボタンが散在する画面を作成する場合、柔軟性の代わりに **addControls()** メソッドを上書きできます。

考慮すべきの追加のシナリオは、たとえば、ユーザーが正しくない製造オーダー ID を入力した場合など、検証エラーが発生した場合にページを再構築する方法です。 **ProcessGuidePageBuilder** 基本クラスは、ユーザー インターフェイスを再構築し、スキャンした値をクリアし、エラー メッセージのあるエラー コントロールを追加するという、既定の動作を実装します。 これは、使用する既定の動作であるため、エラーを処理するコードを追加する必要はありません。

> [!TIP]
> エラー状況のカスタム UI 動作を実装する場合は、1 つまたは複数のメソッド **rebuildFromRequestPage()**、**isErrorState()**、および **reuseRequestPageOnError()** を上書きすることができます。

### <a name="processing-the-user-entered-data-in-the-first-step"></a>最初の手順でユーザーが入力したデータの処理

データの処理は、**ProcessGuideDataProcessorDefault** クラスで行われ、その後、レガシ **WhsRfControlData** クラスが呼び出されます。 この既定の動作を変更する必要はありません。**WhsRfControlData** には、既に **ProdId** フィールを検証するロジックがあるため、これを処理するロジックを記述する必要はありません。 検証ロジックに必要な機能拡張がある場合、**WhsControl** ベースの拡張メカニズムを使用することを検討します。

### <a name="determine-if-the-first-step-is-complete"></a>最初の手順が完全であるかどうかを判断

検証に成功したらを、ステップを完了としてマークします。 これは、基本クラスで行われますが、手順の完了を決定する条件を実装する必要があります。 オーバーライドされた次のメソッドがそれを行います。

``protected final boolean isComplete()
{
    WhsrfPassthrough pass = controller.parmSessionState().parmPass();
    ProdId prodId = pass.lookup(ProcessGuideDataTypeNames::ProdId);
        return (prodId != '');
 }``   

### <a name="step-two-view-order-details-and-confirm"></a>ステップ 2: 注文の詳細を表示して確認

プロセスの 2 番目のステップでは、ユーザーに、注文に関する詳細を含む画面が表示されます。 ユーザーは **OK** ボタンをクリックして製造オーダーの開始を確認するか、**キャンセル** をクリックしてプロセスの開始に戻ることができます。 この例では、ステップ **ProdProcessGuideConfirmProductionOrderStep** とページ ビルダー クラス **ProdProcessGuideConfirmProductionOrderPageBuilder** を指定します。

ProdProcessGuideConfirmProductionOrderStep クラスは、次のようになります。

``[ProcessGuideStepName(classStr(ProdProcessGuideConfirmProductionOrderStep))]
public class ProdProcessGuideConfirmProductionOrderStep extends ProcessGuideStep
{
    protected final ProcessGuidePageBuilderName pageBuilderName()
    {
        return classStr(ProdProcessGuideConfirmProductionOrderPageBuilder);
     }
 }``     

ユーザーはここに値を入力してないため、**isComplete()** メソッドを上書きする必要はありません。 ユーザーが **OK** をクリックすると、ステップが完了します。

ページ ビルダー クラスは、**addDataControls()** メソッドを上書きして 3 つのラベルを追加します。 最初のラベルには、製造オーダー ID が表示され、2 番目には、品目情報 (品目 ID、分析コード、説明など) が表示され、3 番目には数量との測定単位が含まれています。

その後、**addActionControls()** が上書きされ、2 つのボタン (**OK** ボタンと、プロセスをキャンセルしてプロセスの先頭に戻る **Cancel** ボタン) を追加します。

![プロセス ガイド ページ ビルダー コード](media/process-guide-page-builder-code.png)

### <a name="step-3-start-the-production-order"></a>ステップ 3: 製造オーダーを開始する

3 番目のステップでは、製造オーダーの開始のビジネス ロジックを実行します。 このステップは、ユーザー インターフェイスがないという点で前のステップとは少し異なります。 ユーザーが前のステップで **OK** をクリックすると、このステップがサイレントで実行されます。

**ProcessGuideStepWithoutPrompt** 抽象クラスは、そのようなステップの既定の動作を実装します。 したがって、現在のステップは、**ProcessGuideStepWithoutPrompt** クラスを拡張し、**doExecute()** メソッドを上書きする必要があります。

次のコード例は、そのクラスと **doExecute()** メソッドの実装を示しています。 このメソッドは単に、、セッションの状態から注文 ID とユーザー ID を取得し、この製造オーダーを開始するメソッドを呼び出すだけです。

![](media/class-and-method-implementation.png)

例外が発生した場合、フレームワーク例外処理ロジックは、前の手順でプロセスがロールバックされることを保証します。

> [!NOTE]
> **addProcessCompletionMessage()** の呼び出しは、ナビゲーション パラメーターに "作業完了" メッセージを追加します。 このメッセージは、(ユーザー インターフェイスがあると仮定した場合) 次のステップで表示されます。 基本クラスは、このロジックを処理するため、この動作を実現するために特定のコードをプロセス クラスに追加する必要はありません。


### <a name="building-the-navigation-through-the-steps"></a>ステップでのナビゲーションの構築

**ProcessGuideController** 基本クラスは、**ProcessGuideNavigationAgentDefault** クラスのインスタンスを作成します。これは、ソースおよび出力先のステップの簡単なマップである事前に定義されたナビゲーション工順に依存しています。 生産開始シナリオでは、条件分岐がないため、この実装で十分です。 したがって、必要があるのは、**initializeNavigationRoute()** メソッドをオーバーライドしてナビゲーション工順を定義することだけです。

![メソッド コードのオーバーライド](media/override-method-code.png)

条件付き分岐が配置されるプロセスがあります (ユーザーの操作、またはその他の条件に基づく)。 このようなプロセスは、次の操作を行う必要があります。

-   **ProcessGuideNavigationAgent** クラスから継承された特定のナビゲーション エージェントを実装します。

-   現在のステップ、セッションの状態、ユーザーのアクション、または他のロジックに基づいて適切なナビゲーション エージェントのインスタンスを作成するためのロジックを含む、**ProcessGuideNavigationAgentAbstractFactory** クラスから継承された特定のナビゲーション エージェント ファクトリを実装します。

-   必要に応じて、コントローラー クラスで **navigationAgentCreationParameters()** をオーバーライドして、適切なパラメーターを渡します。

-   コントローラーで **navigationAgentFactory()** をオーバーライドして、上で作成したナビゲーション エージェント ファクトリのインスタンスを作成します。

### <a name="action-classes"></a>アクション クラス

アクション クラスはユーザーの操作を表すため、この例では、 **OK** アクションを使用して、アクションの作成方法を表示します。

``[ProcessGuideActionName(#ActionOK)]
public class ProcessGuideOKAction extends ProcessGuideAction
{
    public final str label()
    {
        return "@SYS5473";
     }
     protected final void doExecute()
     {
        step.executeOKAction();
      }
  }``    

クラスは 2 つの抽象メソッドを実装する必要があります。

-   **label()**: この操作に関連付けられているボタン コントロールに表示するためのラベルを返します。

-   **doExecute()**: アクションを実行します。 既に述べたように、**OK** ボタンはステップでコールバックを実行するだけです。 ただし、その他のアクションにはここにより複雑なロジックがある場合があります。

アクションは、**ProcessGuideActionName** 属性に基づいて **SysExtension** フレームワークを使用してインスタンス化されます。 ページ ビルダーのインスタンス化と同様、ステップ クラスは、既定のアクション ファクトリを実装し、それを上書きすることができます。 ページ ビルダーは、次のようにボタン コントロールを追加します。

``_page.addButton(step.createAction(#ActionOK), true);``

これを行うことにより、渡された名前のアクション クラスを作成するようステップに求め、そのアクションをボタンに関連付けます。

### <a name="summary"></a>集計

このトピックで説明したことをすべてまとめるため、プロセスに必要なコードの包括的な概要をここに示します。

1.  **ProdProcessGuideProductionStartController**

    1.  **initialStepName()** を上書きして、最初のステップの名前を指定します。
    2.  **initializeNavigationRoute()** を上書きして、ナビゲーション マップを作成します。

        ![ナビゲーション マップの作成](media/construct-navigation-map.png)

2.  **ProdProcessGuidePromptProductionIdStep**

    1.  **isComplete()** を上書きし、ステップが完了と見なされるタイミングを指定します。
    2.  **pageBuilderName()** を上書きし、使用するページ ビルダーを指定します。

![ページ ビルダーの指定](media/specify-page-builder.png)

3.  **ProdProcessGuidePromptProductionIdPageBuilder**

    1.  **addDataControls()** を上書きし、**製品 ID** テキスト ボックスを追加します。
    2.  **addActionControls()** をオーバーライドして **OK** および **Cancel** ボタンを追加します。

        ![addActionControls のオーバーライド](media/override-add-data-controls.png)

4.  **ProdProcessGuideConfirmProductionOrderStep**

    1.  **pageBuilderName()** を上書きし、使用するページ ビルダーを指定します。

        ![pageBuilderName のオーバーライド](media/override-page-builder-name.png)

3.  **ProdProcessGuideConfirmProductionOrderPageBuilder**

    1.  **addDataControls()** をオーバーライドし、注文、品目、および数量情報ラベルを追加します。

    2.  **addActionControls()** をオーバーライドして **OK** および **Cancel** ボタンを追加します。

        ![addActionControls のオーバーライド](media/override-controls.png)

        > [!NOTE]
        > 品目情報のラベルを生成するために使用される **generateItemInfoForProdId()** メソッドは、このトピックから除外されます。 このメソッドは、品目 ID、説明、および分析コードを取得するいくつかのテーブルを照会します。 **generateItemInfoForProdId()** についてよく理解する場合、ソース コードを確認します。

4.  **ProdProcessGuideStartProductionOrderStep**

    1.  **doExecute()** を上書きして生産プロセスの開始を実行し、プロセスの完了メッセージを追加します。

![ProdProcessGuideStartProductionOrderStep](media/add-process-completion-message.png)

> [!NOTE]
> 多くの一般的なパターン (エラー時の UI の再生成、設定プロセスの完了メッセージ、**OK** および **キャンセル** 動作) がフレームワークに移動された点に注意してください。したがって、エラーの発生しやすい定型コードと、プロセス間で不整合な動作をする危険性を備えた定型コードの両方をアプリケーション開発者が記述しなくてよくなります。 ただし、共通するパスとは異なるシナリオが必要な場合、アプリケーション開発者には、適切なメソッドをオーバーライドするオプションが用意されていますが、その場合、それは明示的なかつ追跡可能な意図的な誤差です。


### <a name="extending-a-business-process"></a>業務プロセスの拡張

これまでのところ、このトピックでは **ProcessGuide** フレームワークを使用して新しいプロセスを作成する方法が強調表示されています。 この最後のセクションでは、このビジネス プロセスを拡張する方法の例をいくつか示します。

### <a name="add-a-step-in-a-flow-using-processguidenavigationagentdefault"></a>フローにおけるステップの追加 (ProcessGuideNavigationAgentDefault を使用)

拡張場所:

-   プロセスの **ProcessGuideController** クラスの子。

拡張方法:

-   コントローラー クラスで **initializeNavigationRoute()** メソッドを拡張し、**ProcessGuideNavigationRoute** クラスで **addFollowingStep()** を呼び出します。

### <a name="add-a-step-in-a-flow-using-custom-navigation-agent"></a>フローにおけるステップの追加 (カスタム ナビゲーション エージェントを使用)

拡張場所:

-   **ProdProcessGuideNavigationAgentFactory/ProdProcessGuideNavigationAgent** の子。

拡張方法:

-   必要なステップの名前を返す **ProcessGuideNavigationAgent** の新しい子クラスを作成します。

-   上で作成したナビゲーション エージェントを条件付きで返す **ProcessGuideNavigationAgentFactory** から派生した新しいクラスを作成します。

-   コントローラー クラスで **navigationAgentFactory()** メソッドを拡張し、上で作成したファクトリを返します。

### <a name="add-a-new-control-in-the-ui-of-an-existing-step"></a>既存のステップの UI で新しいコントロールを追加 

拡張場所:

-   ステップの **ProdProcessGuidePageBuilder** の子。

拡張方法:

-   **addDataControls()** メソッドを拡張し、その他のコントロールを追加します。

### <a name="complete-overhaul-of-the-user-interface-in-an-existing-step"></a>既存のステップでのユーザー インターフェイスの全体的な修正

拡張場所:

-   **ProdProcessGuideStep** の子。

拡張方法:

-   **ProdProcessGuidePageBuilder** クラスの新しい子クラスを作成し、目的のユーザー インターフェイスを実装します。

-   ステップ クラスで **pageBuildeName()** メソッドを拡張し、上で作成したクラスの **ProcessGuidePageBuilderNameAttribute** を返します。

### <a name="alter-logic-when-a-step-is-considered-complete"></a>ステップが完了と見なされたときにロジックを変更します。

拡張場所:

-   **ProdProcessGuideStep** の子。

拡張方法:

-   **isComplete()** メソッドを拡張し、追加ロジックを構築します。
