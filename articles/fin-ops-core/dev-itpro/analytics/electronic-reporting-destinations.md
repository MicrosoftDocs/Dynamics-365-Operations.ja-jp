---
title: 電子申告 (ER) の送信先
description: この記事では、電子申告の送信先の管理、サポートされている送信先のタイプ、およびセキュリティ上の注意事項について説明します。
author: kfend
ms.date: 08/28/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: filatovm
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 7.0.1
ms.custom: 97423
ms.assetid: f3055a27-717a-4c94-a912-f269a1288be6
ms.search.form: DocuType, ERSolutionTable
ms.openlocfilehash: b1bf6289e80769dfe8858f307cbb9b217b42dbb4
ms.sourcegitcommit: f2edc193003564c5bee1747f9c2b800feee342bd
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/29/2022
ms.locfileid: "9360982"
---
# <a name="electronic-reporting-er-destinations"></a>電子申告 (ER) の送信先

[!include [banner](../includes/banner.md)]

各電子レポート (ER) 形式のコンフィギュレーション、および生産物コンポーネント (フォルダやファイル) の出力先をコンフィギュレーションできます。 適切なアクセス権を持っているユーザーは、実行時に送信先の設定を変更することもできます。 この資料では、電子申告の送信先の管理、サポートされている送信先の種類とセキュリティに関する考慮事項について説明します。

ER 形式の構成には、通常少なくとも 1 つの出力のコンポーネント (ファイル) が含まれます。 通常、構成には 1 つのフォルダーまたは複数のフォルダーのいずれかにグループ化された、異なる種類 (たとえば、XML、TXT、XLSX、DOCX、または PDF) の複数のファイル出力コンポーネントが含まれています。 電子申告の送信先管理では、各コンポーネントの実行時に発生する内容を事前に構成することができます。 構成を実行すると、既定では、ファイルを保存または開くためのダイアログ ボックスが表示されます。 同様の動作は、電子申告の構成をインポートし、任意の特定の宛先を構成しない場合にも発生します。 主な出力コンポーネントの送信先が作成されると、その送信先は既定の動作を上書きし、フォルダーまたはファイルは宛先の設定に従って送信されます。

## <a name="availability-and-general-prerequisites"></a>可用性と一般的な前提条件

ER の送信先の機能は、Microsoft Dynamics AX 7.0 (2016 年 2 月) では利用できません。 したがって、次の送信先タイプを使用するには、Microsoft Dynamics 365 for Operations バージョン 1611 (2016 年 11 月) 以降をインストールする必要があります。

- [電子メール](er-destination-type-email.md)
- [アーカイブ](er-destination-type-archive.md)
- [ファイル](er-destination-type-file.md)
- [画面](er-destination-type-screen.md)
- [Power BI](er-destination-type-powerbi.md)

または、次の前提条件のいずれかをインストールできます。 ただし、これらの代替条件により、ER 出力先のエクスペリエンスがさらに制限されることに注意してください。

- Microsoft Dynamics AX アプリケーションのバージョン 7.0.1 (2016 年 5 月)
- [電子申告の送信先管理アプリケーションの修正プログラム](https://fix.lcs.dynamics.com/issue/results/?q=3160213)

また、[印刷](er-destination-type-print.md) 送信先のタイプもあります。 使用するには、Microsoft Dynamics 365 Finance バージョン 10.0.9 (2020 年 4 月) をインストールする必要があります。

## <a name="overview"></a>概要

現在の Finance インスタンスに [インポート](general-electronic-reporting.md#importing-an-er-component-from-lcs-to-use-it-internally) された電子申告構成、および **電子申告コンフィギュレーション** ページで利用可能な形式に対してのみ送信先を設定することができます。 ER の送信先管理の機能は、**組織管理** \> **電子申告** \> **電子申告の送信先** で利用可能です。

### <a name="default-behavior"></a>既定の動作

ER フォーマット構成の既定の動作は、ERフォーマットの開始時に指定された実行タイプによって異なります。

**イントラスタット レポート** ダイアログ ボックスの **バックグラウンドで実行する** クイックタブで、**バッチ処理** オプションを **いいえ** に設定した場合は、ER フォーマットがインタラクティブ モードで直ちに実行されます。 この実行が正常に完了すると、生成された送信ドキュメントがダウンロード可能になります。

**バッチ処理** オプションを **はい** に設定した場合 、ER フォーマットは [バッチ](../sysadmin/batch-processing-overview.md) モードで実行されます。 **ERパラメータ** ダイアログボックスの **バックグラウンドで実行する** タブで、実行時に指定されたパラメータに基づいて、適切なバッチジョブが作成されます。

> [!NOTE]
> ジョブ記述は、ER 形式マッピングの実行について通知します。 また、実行される ER コンポーネントの名前も含まれています。

[![ER 形式の実行。](./media/ER_Destinations-RunInBatchMode.png)](./media/ER_Destinations-RunInBatchMode.png)

このジョブの詳細については、次のいずれかの場所で確認できます：

- **共通** \> **照会** \> **バッチ ジョブ** \> **自分のバッチ ジョブ** に移動し、スケジュールされたジョブの状態を確認します。
- **組織管理** \> **電子レポート** \> **電子レポートジョブ** に移動し、スケジュールされたジョブの状態と完了したジョブの実行結果を確認します。 ジョブの実行が正常に完了したら、**電子レポートジョブ**  ページの **ファイルの表示** を選択して、生成された送信ドキュメントを取得します。

    > [!NOTE]
    > このドキュメントは、現在のジョブ レコードの添付ファイルとして保存され、[ドキュメント管理](../../fin-ops/organization-administration/configure-document-management.md) フレームワークによって制御されます。 このタイプの ER 成果物の格納に使用される [文書タイプ](../../fin-ops/organization-administration/configure-document-management.md#configure-document-types) は、[ER パラメータ](electronic-reporting-er-configure-parameters.md#parameters-to-manage-documents)で構成されています。

- **電子レポート ジョブ** ページで、**ファイルの表示** を選択し、ジョブの実行中に生成されたエラーと警告の一覧を表示します。

    [![ER ジョブリストの確認。](./media/ER_Destinations-ReviewERJobs.png)](./media/ER_Destinations-ReviewERJobs.png)

### <a name="user-configured-behavior"></a>ユーザー構成の動作

**電子申告の送信先** ページで、コンフィギュレーションの既定の動作をオーバーライドできます。 **新規** を選択し、**参照** フィールドで送信先の設定を作成する構成を選択するまで、インポートされた構成はこのページには表示されません。

[![参照フィールドで構成を選択する。](./media/ER_Destinations-SelectFormat.png)](./media/ER_Destinations-SelectFormat.png)

参照を作成した後、参照している ER 形式の各 **フォルダー** または **ファイル** 出力コンポーネントに対して、ファイル送信先を作成できます。

[![ファイル移動先を作成。](./media/ER_Destinations-ConfigureElementDestination.png)](./media/ER_Destinations-ConfigureElementDestination.png)

次に、**送信先の設定** ダイアログ ボックスで、ファイル送信先に対して個別の送信先の有効化および無効化を行えます。 **設定** ボタンは選択したファイルの送信先のすべての送信先を制御するために使用します。 **送信先の設定** ダイアログ ボックスで、 **有効** オプションを設定して各送信先を個別に制御できます。

**バージョン 10.0.9 より前** のバージョンの Finance の場合、**ファイル名** フィールドで選択したフォルダーまたはファイルなどの、同じ形式の各出力コンポーネントに対して、**1 つのファイルの出力先** を作成できます。 ただし、**バージョン 10.0.9 以降** では、同じ形式の出力コンポーネントそれぞれに対して **複数のファイル送信先** を作成できます。

たとえば、この機能を使用して、Excel 形式で送信ドキュメントを生成するために使用されるファイル コンポーネントのファイル送信先をコンフィギュレーションできます。 ER ジョブ アーカイブに元の Excel ファイルを保存するために 1 つの送信先 ([アーカイブ](er-destination-type-archive.md)) をコンフィギュレーションすることができ、同時に Excel ファイルを PDF 形式に [変換](#OutputConversionToPDF) して電子メールで送信するように他の送信先 ([電子メール](er-destination-type-email.md)) をコンフィギュレーションすることができます。

[![1 つの形式要素に対する複数の送信先のコンフィギュレーション。](./media/ER_Destinations-SampleDestinations.png)](./media/ER_Destinations-SampleDestinations.png)

ER 形式を実行すると、その形式のコンポーネントに対して構成されている送信先すべてが常に実行されます。 さらに、Finance **バージョン 10.0.17以降** では、ER の送信先機能が強化され、1 つの ER 形式に対してさまざまな送信先セットを構成できるようになりました。 このコンフィギュレーションは、各セットを特定のユーザー アクションに対してコンフィギュレーション済みとしてマークします。 ER API は [拡張](er-apis-app10-0-17.md) され、ER 形式を実行することでユーザーが実行するアクションを提供できるようになりました。 指定されたアクション コードは、ER の送信先に渡されます。 提供されているアクション コードに応じて、ER 形式のさまざまな出力先を実行できます。 詳細については、[アクション依存の ER 送信先を構成する](er-action-dependent-destinations.md) を参照してください。

## <a name="destination-types"></a>行先タイプ

ER 形式では、現在、次の送信先がサポートされています。 同時にすべてのタイプを有効または無効にできます。 この方法で、何もしないか、コンポーネントを構成済みのすべての送信先に送信します。

- [電子メール](er-destination-type-email.md)
- [アーカイブ](er-destination-type-archive.md)
- [ファイル](er-destination-type-file.md)
- [画面](er-destination-type-screen.md)
- [Power BI](er-destination-type-powerbi.md)
- [印刷](er-destination-type-print.md)

## <a name="applicability"></a>適合性

インポートされた電子申告構成、および **電子申告コンフィギュレーション** ページで利用可能な形式に対してのみ送信先を設定することができます。

> [!NOTE]
> コンフィギュレーションされた送信先は会社固有のものです。 ER 形式を現在の Finance インスタンスの異なる会社で使用する場合、それらの会社ごとに ER 形式の送信先をコンフィギュレーションする必要があります。

選択した形式に対してファイル送信先をコンフィギュレーションする場合、形式全体に対してコンフィギュレーションすることになります。

[![コンフィギュレーション リンク。](./media/ER_Destinations-ConfigurationLink.png)](./media/ER_Destinations-ConfigurationLink.png)

同時に、現在の Finance インスタンスにインポートされた形式の バージョン が複数あることがあります。 それらは、参照フィールドを選択した **時** に提供される **コンフィギュレーション** リンクを選択した場合に表示できます。

[![コンフィギュレーション バージョン。](./media/ER_Destinations-ConfigurationVersions.png)](./media/ER_Destinations-ConfigurationVersions.png)

既定では、コンフィギュエーションされた送信先は、**完了** または **共有** の状態にある ER 形式バージョンを実行した場合にのみ適用されます。 ただし、ER 形式のドラフト バージョンが実行されている場合、コンフィギュレーションされた送信先を使用する必要がある場合があります。 たとえば、形式のドラフト バージョンを変更し、生成された出力がどのように配信されるかテストするためにコンフィギュレーションされた送信先を使用したい場合です。 ドラフト バージョンを実行する時に ER 形式の送信先を適用するには、次の手順に従います。

1. **組織管理** \> **電子申告** \> **構成** の順に移動します。
2. **構成** ページ、アクション ウィンドウ、**構成** タブ、**詳細設定** グループで、**ユーザー パラメーター** を選択します。
3. **ドラフト状態で送信先を使用する** のオプションを **はい** に設定します。

[![ドラフト状態で送信先を使用するオプション。](./media/ER_Destinations-UserSetting1.png)](./media/ER_Destinations-UserSetting1.png)

ER 形式のドラフト バージョンを使用するには、適宜 ER 形式をマークする必要があります。

1. **組織管理** \> **電子申告** \> **構成** の順に移動します。
2. **構成** ページ、アクション ウィンドウ、**構成** タブ、**詳細設定** グループで、**ユーザー パラメーター** を選択します。
3. **実行設定** オプションを **はい** に設定します。

[![実行設定オプション。](./media/ER_Destinations-UserSetting2.png)](./media/ER_Destinations-UserSetting2.png)

この設定を完了した後、**ドラフトの実行** オプションが変更する ER 形式に対して使用可能になります。 このオプションを **はい** に設定し、形式を実行する時に形式のドラフト バージョンの使用を開始することができます。

[![ドラフトの実行オプション。](./media/ER_Destinations-FormatSetting.png)](./media/ER_Destinations-FormatSetting.png)

## <a name="destination-failure-handling"></a><a name="DestinationFailure"></a>送信先失敗の処理

通常、ER 形式は特定の業務プロセスのスコープ内で実行されます。 ただし、ER 形式の実行中に生成される送信ドキュメントの配信は、ときには業務プロセスの一部と見なす必要があります。 この場合、コンフィギュレーションされた送信先に生成された送信ドキュメントの配信が失敗するなら、業務プロセスの実行をキャンセルする必要があります。 適切な ER 送信先をコンフィギュレーションするには、**失敗時に処理を停止** オプションを選択します。

たとえば、仕入先支払処理をコンフィギュレーションして、**ISO20022 口座振替** ER 形式を実行して支払ファイルおよび補足ドキュメント (たとえば、送付状および管理レポート) を生成します。 送付状が電子メールによって正常に配信された場合にのみ支払が正常に処理されたと見なすには、次の図に示すように、適切なファイル送信先の **CoveringLetter** コンポーネントに対する **失敗時に処理を停止** チェック ボックスをオンにする必要があります。 この場合、処理用に選択されている支払の状態が **なし** から **送信済** に変更されるのは、生成された送付状が Finance インスタンスでコンフィギュレーションされた電子メール プロバイダーによって配信用に承認された場合に限られます。

[![ファイル送信先の失敗に対するプロセス処理のコンフィギュレーション。](./media/ER_Destinations-StopProcessingAtDestinationFailure.png)](./media/ER_Destinations-StopProcessingAtDestinationFailure.png)

送信先の **CoveringLetter** コンポーネントに対する **失敗時に処理を停止** チェック ボックスをオフにした場合、支払は送付状が電子メールによって正常に配信されていない場合でも正常に処理されたと見なされます。 たとえば、受取人または送信者の電子メール アドレスが見つからないか正しくないなどの理由で、送付状を送信できない場合でも、その支払の状態は **なし** から **送信済** に変更されます。

## <a name="output-conversion-to-pdf"></a><a name="OutputConversionToPDF"></a> 出力の PDF への変換

PDF への変換オプションを使用して、Microsoft Office (Excel または Word) 形式の出力を PDF 形式に変換することができます。

### <a name="make-pdf-conversion-available"></a>PDF 変換を使用可能にする

現在の Finance インスタンスで PDF 変換オプションを使用可能にするには、**機能管理** ワークスペースを開き、**Microsoft Office 形式から PDF に電子申告送信ドキュメントを変換** 機能を有効にします。

[![機能管理における送信ドキュメントの PDF 変換機能の有効化。](./media/ER_Destinations-EnablePdfConversionFeature.png)](./media/ER_Destinations-EnablePdfConversionFeature.png)

### <a name="applicability"></a>適用性

**バージョン 10.0.18** より前の Finance では、PDF 変換オプションは Office (Excel または Word) 形式で出力の生成に使用する **Excel\\File** コンポーネントに対してのみ有効化できます。 このオプションをオンにすると、Office 形式で生成された出力は自動的に PDF 形式に変換されます。 ただし、**バージョン 10.0.18 以降** では、**Common\\File** タイプのコンポーネントに対してのみこのオプションをオンにすることもできます。

> [!NOTE]
> **Common\\File** タイプの ER コンポーネントの PDF 変換オプションをオンすると表示される警告メッセージに注意してください。 このメッセージは、選択したファイル コンポーネントが実行時に PDF 形式のコンテンツまたは PDF に変換可能なコンテンツを公開することを設計時に保証する方法がないことを通知します。 したがって、選択したファイル コンポーネントが実行時に PDF 形式または PDF に変換可能なコンテンツを公開する場合にのみ、このオプションをオンにする必要があります。
> 
> フォーマット コンポーネントの PDF 変換オプションをオンにした場合、そのコンポーネントが PDF 以外の形式でコンテンツを公開し、公開されたコンテンツを PDF 形式に変換できない場合は、実行時に例外が発生します。 受信したメッセージは、生成されたコンテンツを PDF 形式に変換できないことを通知します。

### <a name="limitations"></a>制限

Finance **バージョン 10.0.9** からは、PDF 変換のオプションはクラウド展開のみで利用可能です。 Finance バージョン **10.0.27** から、[インターネット接続](../user-interface/client-disconnected.md) が有効になっているすべての導入環境で PDF 変換オプションを使用できます。

生成される PDF ドキュメントは最大長 300 ページに制限されます。

Finance **バージョン 10.0.9** では、Excel 出力から生成される PDF ドキュメントでは、横方向のみがサポートされます。 Finance **バージョン 10.0.10** 以降では、ER 送信先を構成する際に、Excel 出力から生成される PDF ドキュメントの [印刷の向きを指定](#SelectPdfPageOrientation) することができます。

埋め込みフォントを含まない出力の変換には、Windows オペレーティング システム共通のシステム フォントのみが使用されます。

### <a name="resources"></a>リソース

Finance バージョン 10.0.29 より前では、PDF 変換は現在の Finance インスタンスの外部でのみ実行できます。 生成されたファイルは Finance から換算サービスに送信され、そのサービスは変換されたドキュメントを返しました。 ただし、バージョン **10.0.29 以降** では、**Microsoft Office 形式から PDF に電子申告送信ドキュメントを変換する** 機能に加えて、**アプリケーション リソースを使用して Word から PDF 形式に CBD ドキュメントを変換する** 機能を有効にすることができます。 この機能により、現在の Finance インスタンスでアプリケーション サーバー リソースを使用して、生成した Word ドキュメントをローカルで PDF 形式に変換できます。 

**アプリケーション リソースを使用して Word から PDF 形式に CBD ドキュメントを変換する** 機能を有効にした場合のローカル PDF 変換の利点は次のとおりです:

- 生成される PDF ドキュメントは、ページ数の上限に [制限](#limitations) されません。
- 変換される Word ドキュメントには、[多数のコンテンツ コントロール](https://fix.lcs.dynamics.com/Issue/Details?bugId=647877&dbType=3) を含めることができます。
- インターネット接続は、オンプレミスの展開では必要ありません。

### <a name="use-the-pdf-conversion-option"></a>PDF 変換オプションの使用

ファイル送信先に対して PDF 変換を有効にするには、**PDF に変換** チェック ボックスをオンにします。

[![ファイル送信先への PDF 変換の有効化。](./media/ER_Destinations-TurnOnPDFConversion.png)](./media/ER_Destinations-TurnOnPDFConversion.png)

### <a name=""></a><a name="SelectPdfPageOrientation">PDF 変換で使用するページの向きを選択する</a>

ER の構成を Excel 形式で生成し、PDF 形式に変換する場合は、PDF ドキュメントの印刷の向きを指定できます。 ファイルの保存先の指定時にExcel フォーマットを指定し、 **PDF に変換する** チェック ボックスを選択して PDF 変換を有効化すると、**ページの向き** フィールドが **PDF conversion settings** ファストタブで利用可能になります。 **ページの方向** フィールドで、ページの向きを選択します。

[![PDF 変換の対象とするページの方向を選択する。](./media/ER_Destinations-SelectPDFConversionPageOrientation.png)](./media/ER_Destinations-SelectPDFConversionPageOrientation.png)

PDF の印刷の向きを選択するオプションを使用するには、Finance バージョン 10.0.10 以降のインストールが必要となります。 Finance の **バージョン 10.0.23 以前** では、このオプションでは、次のページの向きが選択できます。

- 縦
- 横

Excel 形式で作成され、PDF 形式に変換された送信文書のすべてのページに、選択したページの向きが適用されます。

ただし、**バージョン 10.0.23** 以降では、ページ方向のオプションの一覧が次のように拡張されています:

- 縦
- 横
- ワークシートに固有

**ワークシート固有** のオプションを選択すると、生成された Excel ブックのすべてのワークシートが、使用する Excel テンプレートのこのワークシート用に構成されたページの向きを使用してPDFに 変換されます。 そのため、最終的には縦長のページと横長のページを含む PDF 文書が作成されます。 

Word 形式の ER 構成を PDF 形式に変換した場合、PDF 文書のページの向きは常に Word 文書のものが採用されます。

## <a name="output-unfolding"></a>結果の展開

ER フォーマットの **フォルダ** コンポーネントの配信先を設定すると、そのコンポーネントの出力を設定した配信先への配信方法を指定できます。

### <a name="make-output-unfolding-available"></a>結果の展開を可能にする

現在の Finance インスタンスで出力展開オプションを使用できるようにするには、**機能管理** ワークスペースを開き、**ER の出力先を構成してフォルダのコンテンツを別のファイルとして送信する** 機能をオンにします。

### <a name="applicability"></a>適用性

出力のアンフォールディング オプションは、**フォルダー** タイプのフォーマット コンポーネントに対してのみ構成できます。 **フォルダー** コンポーネントの構成を開始すると、**電子報告書の送信先** ページで **全般** クイック タブが利用可能になります。 

### <a name="use-the-output-unfolding-option"></a>出力を変更するオプションの使用

**一般** クイック タブの **名前を付けて送信** フィールドで 、次のいずれかの値を選択します:

- **ZIP アーカイブ** - 生成されたファイルを zip ファイルとして配信します。
- **ファイルの分割** - 生成されたzipファイルのすべてのファイルを個別のファイルとして配信します。

    > [!NOTE]
    > **個別のファイル** を選択 した場合、生成された出力はZIP状態でメモリに収集されます。 そのため、実際のファイルサイズがこの上限を超える可能性がある場合には、ZIP 出力に対して最大の[ファイルサイズの上限](er-compress-outbound-files.md)が適用されます。 生成される出力のサイズがかなり大きくなることが予想される場合は、この値を選択することをお勧めします。

[![フォルダ形式コンポーネントの出力先を構成する。](./media/er_destinations-set-unfolding-option.png)](./media/er_destinations-set-unfolding-option.png)

### <a name="limitations"></a>制限

ネストした他の **フォルダー** コンポーネントを含む **フォルダー** コンポーネントの **名前を付けて送信** フィールドを **個別のファイル** に設定した場合、その設定はネストした **フォルダー** コンポーネントには設定の変更が適用されません。

## <a name="change-page-layout-properties-of-a-template"></a><a name="change-page-layout-properties-of-a-template"></a> テンプレートのページ レイアウト プロパティの変更

レポート生成用にテンプレートを Microsoft Office (Excel または Word) 形式で使用するように設計されている ER 書式コンポーネント用の ER 出力先を構成できます。 この形式の所有者ではない場合に、形式のテンプレートのページ レイアウト プロパティを変更する必要がある場合、バージョン 10.0.29 より前のバージョンの Finance で、派生するフォーマットを作成し、テンプレートのプロパティを変更する必要があります。 次に、派生形式の構成を管理する必要があります。 ただし、バージョン 10.0.29 以降では、派生形式の構成を作成および管理しなくてすむように、テンプレートのページ レイアウト プロパティを実行時に変更できます。 これを行うには、必要なプロパティを、設定済みの ER 送信先の一部として設定します。 ER 形式を実行し、特定のページ レイアウト プロパティを使用するように構成されている ER 送信先を実行すると、実行される送信先のページ レイアウト プロパティの値が使用しているテンプレートに適用され、元のテンプレートのプロパティが置換されます。 同じ形式のコンポーネントに対してさまざまな送信先を設定し、使用中のテンプレートに対して異なるページ レイアウト プロパティを構成できます。

次のプロパティは、Excel または Word 形式のテンプレートを使用するように設計されている形式コンポーネントに対して ER 送信先で構成できます。

- ページの向き
    - 縦
    - 横
- 紙のサイズ
    - A3
    - A4
    - A5
    - B4
    - B5
    - Executive
    - 法的情報
    - Letter
    - Statement
    - Tabloid
- ページ余白
    - 上
        - ヘッダー
    - 下
        - フッター
    - 左
    - 右

> [!NOTE]
> PDF 変換が構成されている場合、この方法で構成されたテンプレートの印刷の向きは、[PDF 変換の印刷の向き](#select-a-page-orientation-for-pdf-conversion)に揃える必要があります。

ページの余白を設定するには、長さの単位を選択する必要があります。

- インチ
- センチメートル
- ミリメートル

![[電子申告の送信先] ページのページ レイアウト プロパティを設定します。](./media/er_destinations-set-page-layout-properties.png)

> [!TIP]
> 余白の値はセンチメートルで示され、小数点以下桁数が複数に指定されている場合、実行時に小数点以下 1 桁の最も近い値に丸められます。
>
> 余白の値はミリメートルで示され、小数点以下桁数で指定されている場合、Excel の実行時に小数点なしの最も近い整数に丸められます。
>
> 余白の値はミリメートルで示され、小数点以下桁数が複数に指定されている場合、Word の実行時に小数点 1 桁の最も近い値に丸められます。

## <a name="security-considerations"></a>セキュリティ上の注意事項

電子申告の送信先への権限と職務の 2 種類が使用されます。 1 つのタイプは、法人に対して構成されている送信先をメンテナンスする機能全体を制御します (つまり、**電子申告の送信先** ページへのアクセスを制御します)。 その他のタイプは、実行時に、ER の開発者または ER 機能コンサルタントが構成する送信先の設定を上書きするアプリケーション ユーザーの機能を制御します。

| ロール (AOT 名)                     | ロール名                                  | 職務権限 (AOT 名)                     | 職務権限名                                                        |
|-------------------------------------|--------------------------------------------|-------------------------------------|------------------------------------------------------------------|
| 電子申告開発者                         | 電子申告開発者             | 電子申告フォーマット送信先構成        | 電子申告フォーマットの宛先を構成                |
| 電子申告機能コンサルタント              | 電子申告機能コンサルタント | 電子申告フォーマット送信先構成        | 電子申告フォーマットの宛先を構成                |
| 買掛金勘定支払係    | 買掛金勘定支払係            | ERFormatDestinationRuntimeConfigure | 実行時に電子申告フォーマットの宛先を構成 |
| 買掛金勘定支払係 | 売掛金勘定支払係         | ERFormatDestinationRuntimeConfigure | 実行時に電子申告フォーマットの宛先を構成 |

> [!NOTE]
> 前の職務には 2 つの権限を使用します。 これらの権限は、対応する職務として **ERFormatDestinationConfigure** と **ERFormatDestinationRuntimeConfigure** という、同じ名前を持っています。

## <a name="frequently-asked-questions"></a>よく寄せられる質問

### <a name="i-have-imported-electronic-configurations-and-i-see-them-on-the-electronic-reporting-configurations-page-but-why-dont-i-see-them-on-the-electronic-reporting-destinations-page"></a>電子構成をインポートし、それらは電子申告の構成ページで表示されます。 なぜ電子申告の送信先ページに表示されないのですか。

**新規** を選択し、**参照** フィールドで構成を選択していることを確認してください。 **電子申告の送信先** ページには、送信先が構成されている構成のみが表示されます。

### <a name="is-there-any-way-to-define-which-microsoft-azure-storage-account-and-azure-blob-storage-are-used"></a>どの Microsoft Azure ストレージ アカウントと Azure BLOB ストレージが使用されているかを定義する方法はありますか?

一連番号 ドキュメント管理システムに定義され、使用される既定の Microsoft Azure BLOB ストレージを使用します。

### <a name="what-is-the-purpose-of-the-file-destination-in-the-destination-settings-what-does-that-setting-do"></a>出力先設定のファイルの出力先の目的は何ですか。 その設定では何をしますか。

**ファイル** の送信先は、対話モードで ER 形式を実行するときに Web ブラウザーのダイアログ ボックス を制御するために使用されます。 この送信先を有効にした場合、または構成に送信先が定義されていない場合は、出力ファイルが作成された後に開くまたは保存ダイアログ ボックスが Web ブラウザーに表示されます。

### <a name="can-you-give-an-example-of-the-formula-that-refers-to-a-vendor-account-that-i-can-send-email-to"></a>電子メールを送信できる仕入先に参照するフォーミュラの例をあげてください。

フォーミュラは電子申告の構成に固有です。 たとえば、ISO 20022 クレジット転送の構成に使用する場合、**'$PaymentsForCoveringLetter'.Creditor.Identification.SourceID** または **model.Payments.Creditor.Identification.SourceID** を使用して関連付けられている仕入先のアカウントを取得します。

### <a name="one-of-my-format-configurations-contains-multiple-files-that-are-grouped-into-one-folder-for-example-folder1-contains-file1-file2-and-file3-how-do-i-set-up-destinations-so-that-folder1zip-isnt-created-at-all-file1-is-sent-by-email-file2-is-sent-to-sharepoint-and-i-can-open-file3-immediately-after-the-configuration-is-run"></a>1 つの形式コンフィギュレーションには、1 つのフォルダーにグループ化された複数のファイルが含まれています (たとえば、フォルダー 1 にファイル 1、ファイル 2、ファイル 3 が含まれる)。 Folder1.zip は全く作成されず、ファイル 1 は電子メールで送信され、ファイル 2 は SharePoint に送信され、コンフィギュレーションを実行した後すぐにファイル 3 を開くには、どのように出力先を設定したらよいですか。

まず、ER の構成で利用可能な形式である必要があります。 前提条件に一致している場合、**電子申告の送信先** ページを開き、この構成に新しい参照を作成します。 出力の各コンポーネントに 1 つずつ、4 つの出力先が必要です。 最初のファイルの出力先を作成し、**フォルダー** のように名前を付け、構成でフォルダーを表すファイル名を選択します。 それから **設定** を選択し、すべての出力先が無効になっているかどうかを確認します。 このファイルの出力先にはフォルダーは作成されません。 既定では、ファイルと親フォルダーの階層構造の依存関係のため、ファイルは同じように動作します。 つまり、それらはどこにも送信されません。 既定動作を上書きするには、各ファイルに 1 つずつ、ファイルの出力先をさらに 3 つ作成する必要があります。 それぞれの出力先の設定では、ファイルが送信される出力先を有効にする必要があります。

## <a name="additional-resources"></a>追加リソース

[電子申告 (ER) の概要](general-electronic-reporting.md)

[アクション依存の ER 送信先を構成する](er-action-dependent-destinations.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
