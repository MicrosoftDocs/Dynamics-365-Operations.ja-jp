---
title: "電子申告の送信先"
description: "各電子レポート (ER) 形式のコンフィギュレーション、および生産物コンポーネント (フォルダやファイル) の出力先をコンフィギュレーションできます。 適切なアクセス権が与えられているユーザーは、実行時に送信先の設定を変更することもできます。 この資料では、電子申告の送信先の管理、サポートされている送信先の種類とセキュリティに関する考慮事項について説明します。"
author: ShylaThompson
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
ms.search.form: DocuType, ERSolutionTable
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 97423
ms.assetid: f3055a27-717a-4c94-a912-f269a1288be6
ms.search.region: Global
ms.author: mrolecki
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 7.0.1
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: 5fb008420f82abd7983ee26854f84330705c0c01
ms.contentlocale: ja-jp
ms.lasthandoff: 05/25/2017


---

# <a name="electronic-reporting-destinations"></a>電子申告の送信先

[!include[banner](../includes/banner.md)]


各電子レポート (ER) 形式のコンフィギュレーション、および生産物コンポーネント (フォルダやファイル) の出力先をコンフィギュレーションできます。 適切なアクセス権が与えられているユーザーは、実行時に送信先の設定を変更することもできます。 この資料では、電子申告の送信先の管理、サポートされている送信先の種類とセキュリティに関する考慮事項について説明します。

電子申告 (ER) 形式の構成には、通常少なくとも 1 つの出力のコンポーネント (ファイル) が含まれます。 通常、構成には 1 つのフォルダーまたは複数のフォルダーのいずれかにグループ化された、異なる種類 (たとえば、XML、TXT、または XLSX) の複数のファイル出力コンポーネントが含まれています。 電子申告の送信先管理では、各コンポーネントの実行時に発生する内容を事前に構成することができます。 既定では、構成を実行すると、ファイルを保存または開くためのダイアログ ボックスが表示されます。 同様の動作は、電子申告の構成をインポートし、任意の特定の宛先を構成しない場合にも使用されます。 主な出力コンポーネントの送信先が作成されると、その送信先は既定の動作を上書きし、フォルダーまたはファイルは宛先の設定に従って送信されます。

## <a name="availability-and-general-prerequisites"></a>可用性と一般的な前提条件
電子申告の宛先の機能は、Microsoft Dynamics 365 for Operations 7.0 (2016 年 2 月) のリリースでは利用できません。 したがって、このトピックに記載されているすべての機能を使用するには Microsoft Dynamics 365 for Operations (2016 年 11 月リリース) をインストールする必要があります。 または、次の前提条件のいずれかをインストールできます。 ただし、これらの代替条件は、ER 出力先のエクスペリエンスがさらに制限されることに注意してください。

-   Microsoft Dynamics 365 for Operations application version 7.0.1 (2016 年 5 月)
-   電子申告宛先管理[アプリケーションの修正プログラム](https://fix.lcs.dynamics.com/issue/results/?q=3160213)

インポートされた電子申告構成、および [**電子申告コンフィギュレーション**] ページで利用可能な形式に対してのみ送信先を設定することができます。

## <a name="overview"></a>概要
電子申告の送信先の管理機能は、[**組織管理**] &gt; [**電子申告**] で利用できます。 ここでは、構成の既定の動作を上書きできます。 [**新規**] をクリックし、[**参照**] フィールドで送信先の設定を作成する構成を選択するまで、インポートされた構成はここに表示されません。。

[![参照フィールドで構成を選択する](./media/ger-destinations-2-1611-1024x574.jpg)](./media/ger-destinations-2-1611.jpg) 

参照を作成した後は、各フォルダーまたはファイルにファイルの保存先を作成できます。 

[![ファイル移動先を作成](./media/ger-destinations-1611-1024x586.jpg)](./media/ger-destinations-1611.jpg)

**注:** [**ファイル名**] フィールドで選択したフォルダーまたはファイルなどの同じ形式の各出力コンポーネントに対して、1 つのファイルの出力先を作成できます。 [**送信先の設定**] ダイアログ ボックスで、ファイル送信先に対して個別の送信先を有効および無効にできます。 [**設定**] ボタンは選択したファイルの送信先のすべての送信先を制御するために使用します。 [**送信先の設定**] ダイアログ ボックスで、[**有効**] オプションを設定して各送信先を個別に制御できます。

[![移動先設定ダイアログ ボックス](./media/ger-destinations-settings-1611-1024x589.jpg)](./media/ger-destinations-settings-1611.jpg)

## <a name="destination-types"></a>送信先タイプ
さまざまな種類の送信先がサポートされています。 同時にすべてのタイプを有効または無効にできます。 この方法で、何もしないか、コンポーネントを構成済みのすべての送信先に送信します。 次のセクションでは、サポートされている送信先について説明します。

### <a name="email-destination"></a>電子メールの送信先

[**有効**]を[**はい**]に設定し、出力ファイルを電子メールで送信します。 このオプションを有効にすると、電子メールの受信者を指定して、電子メールの件名および本文を編集できます。 電子メールの件名および本文の定型文を設定したり、ER フォーミュラを使用して電子メールのテキストを動的に作成したりできます。 2 つの方法で ER の電子メール アドレスを構成できます。 構成は、Dynamics 365 for Operations の印刷管理機能での入力と同じ方法で入力できます。 または、フォーミュラでの ER コンフィギュレーションの直接参照を使用して電子メール アドレスを解決できます。

### <a name="email-address-types"></a>電子メール アドレス タイプ

[**To**] や [**Cc**] フィールドの [**編集**] をクリックすると、[**電子メールの送信先**] ダイアログ ボックスが表示されます。 使用する電子メール アドレス タイプを選択できます。

[![ダイアログ ボックスへの電子メール](./media/ger-destinations-email-1-1611-1024x588.jpg)](./media/ger-destinations-email-1-1611.jpg)

#### <a name="print-management"></a>印刷管理

[**管理電子メールの印刷**] タイプを選択する場合、[**To**] フィールドに固定の電子メール アドレスを入力できます。 固定されていない電子メール アドレスを使用するには、ファイルの送信先の電子メール ソース タイプを選択する必要があります。 **顧客**、**仕入先**、**見込顧客**、**連絡先**、**競合他社**、**作業者**、**申請者**、**見込み仕入先**、**不許可仕入先**の値がサポートされます。 電子メール ソース タイプを選択したら、[**電子メール ソース**] フィールドの横のボタンを使用して、**フォーミュラ デザイナー **フォームを開きます。 このフォームを使用して、電子メールの送信先に選択した関係者のアカウントを表すフォーミュラを関連付けられます。

[![印刷管理電子メールタイプの構成](./media/ger-destinations-email-2-1611-1024x588.jpg)](./media/ger-destinations-email-2-1611.jpg) 

フォーミュラは電子申告の構成に固有であることに注意してください。 [**フォーミュラ**] フィールドで、顧客または仕入先の関係者タイプにドキュメント固有の参照を入力します。 入力せずに、顧客または仕入先を表すデータ ソース ノードを検索でき、フォーミュラを更新するには [**データ ソースの追加**] ボタンをクリックします。 たとえば、ISO 20022 の口座振替のコンフィギュレーションを使用する場合、仕入先を表すノードは、**'$PaymentsForCoveringLetter'.Creditor.Identification.SourceID** です。 それ以外の場合は、**DE-001** など任意の文字列値を入力してフォーミュラを保存します。

[![計算式デザイナー](./media/ger_formuladesignerfordestination-1024x541.jpg)](./media/ger_formuladesignerfordestination.jpg)

[**電子メールの送信先**] ダイアログ ボックスで、[**電子メール ソース**] フィールドの横にあるごみ箱ををクリックして、電子メール ソースのフォーミュラを完全に削除します。 または、フォーミュラ デザイナーを開いて、以前に保存されたフォーミュラを変更します。 電子メール アドレスを割り当てるには、[**編集**] をクリックして、[**電子メール アドレスの割り当て**] ダイアログ ボックスを開きます。

[![電子メールの宛先用に電子メール アドレスを割り当てる](./media/ger-destinations-email-3-1611-1024x587.jpg)](./media/ger-destinations-email-3-1611.jpg)

#### <a name="configuration-email"></a>コンフィギュレーション電子メール

使用するコンフィギュレーションが電子メール アドレスを表すデータ ソースにノードを持つ場合にこの電子メール タイプを使用します。 フォーミュラ デザイナーでデータ ソースと機能を使用して、正しく書式設定された電子メール アドレスを取得できます。

[![電子メールの宛先用に電子メールのデータ ソースを割り当てる](./media/ger-destinations-email-4-1611-1024x587.jpg)](./media/ger-destinations-email-4-1611.jpg) 

**注:**Simple Mail Transfer Protocol (SMTP) サーバーを構成し、利用可能にする必要があります。 SMTP サーバーは、Dynamics 365 for Operations の [**システム管理**] &gt; [**セットアップ**] &gt; [**電子メール**] &gt; [**電子メール パラメーター**] で指定できます。

### <a name="archive-destination"></a>アーカイブ先

Microsoft Azure ストレージまたは Microsoft SharePoint フォルダーに出力を送信するには、このオプションを使用できます。 [**有効**] を [**はい**] に設定し、選択したドキュメント タイプで定義されている変換先に出力を送信します。 グループが**ファイル**に設定されているドキュメントタイプのみ選択できます。 ドキュメント タイプを [**組織管理**] &gt; [**ドキュメント管理**] &gt; [**ドキュメント タイプ**] で定義します。 電子申告の送信先への構成は、ドキュメント管理システムの構成と同じです。

[![ドキュメント タイプ ページ](./media/ger_documenttypefile-1024x542.jpg)](./media/ger_documenttypefile.jpg) 

場所は、ファイルの保存場所を決定します。 [**アーカイブ**] 先を有効にすると、コンフィギュレーション実行の結果をジョブ アーカイブに保存できます。 結果は、[**組織管理**] &gt; [**電子申告**] &gt; [**電子申告アーカイブ済ジョブ**] で表示できます。 **注記:** ジョブ アーカイブのドキュメント タイプは、Dynamics 365 for Operations の [**組織管理**] &gt; [**ワークスペース**] &gt; [**電子申告**] &gt; [**電子申告のパラメーター**] で選択できます。

#### <a name="sharepoint"></a>SharePoint

指定された SharePoint フォルダーにファイルを保存することができます。 既定の SharePoint サーバーを [**SharePoint**] タブの、[**組織管理**] &gt; [**ドキュメント管理**] &gt; [**ドキュメント管理パラメーター**] で定義します。 SharePoint フォルダーを構成した後、ドキュメント タイプでの電子申告の出力の保存先フォルダーとして選択できます。 

[![SharePoint フォルダーを選択する](./media/ger_sharepointfolderselection-1024x543.jpg)](./media/ger_sharepointfolderselection.jpg) 

#### <a name="azure-storage"></a>Azure ストレージ

ドキュメント タイプの場所を**アーカイブ ディレクトリ**に設定すると、Azure ストレージにファイルを保存することができます。

### <a name="file-destination"></a>ファイルの送信先

[**有効**] を [**はい**] に設定すると、コンフィギュレーションの実行が終了したときに、[開く] または [保存] のダイアログ ボックスが表示されます。

### <a name="screen-destination"></a>画面出力先

[**有効**] を [**はい**] に設定すると、出力のプレビューが作成されます。 ブラウザー ウィンドウで直接 XML、TXT、PDF などの一部のファイル タイプを表示できます。 Microsoft Excel や Microsoft Word などの他のファイル タイプについては、Microsoft Office Online サービスが使用されます。

### <a name="power-bi-destination"></a>Power BI 出力先

[**有効**] を [**はい**] に設定し、ER コンフィギュレーションを使用して Dynamics 365 for Operations のインスタンスから Microsoft Power BI サービスへのデータ転送を調整します。 転送されたファイルは、その目的にコンフィギュレーションされている Microsoft SharePoint Server インスタンスに保存されます。 詳細については、「[Dynamics Online 365 からデータを Power BI に提供する電子申告コンフィギュレーションを使用する](general-electronic-reporting-report-configuration-get-data-powerbi.md)」を参照してください。 **ヒント:** 既定の動作を上書きする (つまり、構成のダイアログ ボックス) には、送信先の参照および主な出力コンポーネントのファイル保存先を作成し、すべての送信先を無効にします。

## <a name="security-considerations"></a>セキュリティ上の注意事項
電子申告の送信先への権限と職務の 2 種類が使用されます。 1 つのタイプは、法人に対して構成されている全体の送信先を維持する機能を制御します (つまり、[**電子申告の送信先**] ページへのアクセスを制御します)。 その他のタイプは、実行時に、電子申告の開発者または電子申告機能コンサルタントで構成されている送信先の設定を上書きするアプリケーション ユーザーの機能を制御します。

| ロール (AOT 名)                     | ロール名                                  | 職務権限 (AOT 名)                     | 職務権限名                                                        |
|-------------------------------------|--------------------------------------------|-------------------------------------|------------------------------------------------------------------|
| 電子申告開発者                         | 電子申告開発者             | 電子申告フォーマット送信先構成        | 電子申告フォーマットの宛先を構成                |
| 電子申告機能コンサルタント              | 電子申告機能コンサルタント | 電子申告フォーマット送信先構成        | 電子申告フォーマットの宛先を構成                |
| 買掛金勘定支払係    | 買掛金勘定支払係            | ERFormatDestinationRuntimeConfigure | 実行時に電子申告フォーマットの宛先を構成 |
| 買掛金勘定支払係 | 売掛金勘定支払係         | ERFormatDestinationRuntimeConfigure | 実行時に電子申告フォーマットの宛先を構成 |

**注:**前の職務には 2 つの権限を使用します。 これらの権限は、対応する職務として **ERFormatDestinationConfigure**と**ERFormatDestinationRuntimeConfigure** という、同じ名前を持っています。

## <a name="frequently-asked-questions"></a>よく寄せられる質問
### <a name="i-have-imported-electronic-configurations-and-i-see-them-on-the-electronic-reporting-configurations-page-but-why-dont-i-see-them-on-the-electronic-reporting-destinations-page"></a>電子構成をインポートし、それらは電子申告の構成ページで表示されます。 なぜ電子申告の送信先ページに表示されないのですか。

[**新規**] をクリックし、[**参照**] フィールドで構成を選択していることを確認してください。 [**電子申告の送信先**] ページでは、送信先が構成されている構成のみを確認できます。

### <a name="is-there-any-way-to-define-which-azure-storage-account-and-azure-blob-storage-are-used"></a>どの Azure ストレージ アカウントと Azure BLOB ストレージが使用されているかを定義する方法はありますか。

一連番号 ドキュメント管理システムに定義され、使用される既定の Azure BLOB ストレージを使用します。

### <a name="what-is-the-purpose-of-the-file-destination-in-the-destination-settings-what-does-that-setting-do"></a>出力先設定のファイルの出力先の目的は何ですか。 その設定では何をしますか。

[**ファイル**] 出力先はダイアログ ボックスを制御するために使用します。 この出力先を有効にした場合、または構成に出力先が定義されていない場合は、出力ファイルが作成された後に [保存] または [開く] ダイアログ ボックスが表示されます。

### <a name="can-you-give-an-example-of-the-formula-that-refers-to-a-vendor-account-that-i-can-send-email-to"></a>電子メールを送信できる仕入先に参照するフォーミュラの例をあげてください。

フォーミュラは電子申告の構成に固有です。 たとえば、ISO 20022 クレジット転送の構成に使用する場合、**'$PaymentsForCoveringLetter'.Creditor.Identification.SourceID** または **model.Payments.Creditor.Identification.SourceID** を使用して関連付けられている仕入先のアカウントを取得します。

### <a name="one-of-my-format-configurations-contains-multiple-files-that-are-group-into-one-folder-for-example-folder1-contains-file1-file2-and-file3-how-do-i-set-up-destinations-so-that-folder1zip-isnt-created-at-all-file1-is-sent-by-email-file2-is-sent-to-sharepoint-and-i-can-open-file3-immediately-after-the-configuration-is-run"></a>形式のコンフィギュレーションの 1 つには、1 つのフォルダーにグループ化された複数のファイルが含まれています (たとえば、フォルダー 1 にファイル 1、ファイル 2、ファイル 3 が含まれる)。 Folder1.zip は全く作成されず、ファイル 1 は電子メールで送信され、ファイル 2 は SharePoint に送信され、構成を実行した後すぐにファイル 3 を開くには、どのように出力先を設定したらよいですか。

前提条件では、電子申告の構成で利用可能な形式である必要があります。 自分の形式を持っている場合、[**電子申告の送信先**] ページを開き、この構成に新しい参照を作成します。 出力の各コンポーネントに 1 つずつ、4 つの出力先が必要です。 最初のファイルの出力先を作成し、[**フォルダー**] のように名前を付け、構成で、フォルダーを表すファイル名を選択します。 それから [**設定**] をクリックし、すべての出力先が無効になっているかどうかを確認します。 このファイルの出力先にはフォルダーは作成されません。 既定では、ファイルと親フォルダーの階層構造の依存関係のため、ファイルは同じように動作します。 つまり、それらはどこにも送信されません。 既定動作を上書きするには、各ファイルに 1 つずつ、ファイルの出力先をさらに 3 つ作成する必要があります。 それぞれの出力先の設定では、ファイルが送信される出力先を有効にする必要があります。

# <a name="see-also"></a>参照

[電子申告の概要](general-electronic-reporting.md)




