---
title: 受領書フォーマットを設定しデザインします
description: この記事は、フォーム レイアウトを変更して、レシート、請求書、およびその他の文書の印刷方法を制御する方法について説明します。 Dynamics 365 Commerce には、さまざまな種類のフォーム レイアウトを簡単に作成および変更するフォーム レイアウト デザイナーが用意されています。
author: BrianShook
ms.date: 09/16/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: RetailFormLayout
audience: Application User
ms.reviewer: josaw
ms.custom: 57841
ms.assetid: e530dd8e-95e2-4021-90bd-ce1235f9e250
ms.search.region: global
ms.search.industry: Retail
ms.author: brshoo
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: dac0ad75ff35367b5d6ac84c75c68e22e2cb0cb1
ms.sourcegitcommit: f4823a97c856e9a9b4ae14116a43c87f9482dd90
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/09/2021
ms.locfileid: "7779404"
---
# <a name="set-up-and-design-receipt-formats"></a>受領書フォーマットを設定しデザインします

[!include [banner](includes/banner.md)]

この記事は、フォーム レイアウトを変更して、レシート、請求書、およびその他の文書の印刷方法を制御する方法について説明します。 Dynamics 365 Commerce には、さまざまな種類のフォーム レイアウトを簡単に作成および変更するフォーム レイアウト デザイナーが用意されています。

> [!IMPORTANT]
> Retail Modern POS と Cloud POS からレシートやその他の文書を印刷するために、フォーム レイアウトおよびレシート プロファイルを設定する必要があります。 レシート プロファイルに複数のフォーム レイアウトを含めることができます。 ハードウェア プロファイルを変更して、プリンタにレシート プロファイルを割り当てることができます。

## <a name="set-up-a-receipt-format"></a>受領書フォーマットの設定

1. **Retail とコマース** &gt; **チャネル設定** &gt; **POS 設定** &gt; **POS** &gt; **受領書フォーマット** をクリックします。
2. **受領書フォーマット** ページにて、**新規** をクリックし、新しいフォーム レイアウトを作成するか、既存のフォーム レイアウトを選択します。
3. **受領書フォーマット** フィールドで、フォーム レイアウトの ID を入力して、このレイアウトを使用するレシート タイプを選択します。 また、**タイトル** フィールドにレシートの説明と短縮名を入力することもできます。
4. **概要** クイック タブで、印刷動作を定義するオプションを選択します。

    - **常に印刷する** – 必要に応じて、レシートが自動的に印刷されます。
    - **印刷しない** – レシートは印刷されません。
    - **ユーザーに確認する** – ユーザーはレシートを印刷するように求められます。
    - **必要時** – このオプションは、ギフト レシートにのみ使用されます。 ギフト レシートが必要な場合は、このオプションを選択すると、ユーザーは **変更** ページからギフト レシートを印刷できます。

## <a name="print-images"></a>画像の印刷

レシート デザイナーには **ロゴ** 変数 が含まれます。 この変数を使って、レシートに印刷する画像を指定することができます。 **ロゴ** 変数を使用して領収書に印刷する画像は、モノクロのビットマップ(.bmp)ファイルタイプでなければなりません。 レシート デザイナーにビットマップ画像が指定されているにもかかわらず、レシートをプリンターに送信しても印刷されない場合は、以下のような問題が考えられます:

- ファイル サイズが大きすぎるか、画像のピクセル サイズがプリンターに対応していません。 この場合、画像ファイルの解像度や分析コードを小さくしてください。
- 販売時点管理 (OPOS) 用オブジェクトのリンクと埋め込みのプリンタ ドライバによっては、ハードウェア ステーションがロゴ画像を印刷するときに使用する **PrintMemoryBitmap** 方式が実装されていないものがあります。 この場合は、専用または共有ハードウェア ステーションの **HardwareStation.Extension.config** ファイルに以下のフラグを追加してみてください:

    `<add name="HardwareStation.UsePrintBitmapMethod" value="true"/>`

## <a name="design-a-receipt-format"></a>受領書フォーマットのデザイン

フォーム レイアウト デザイナーを使用して、フォーム文書のレイアウトをグラフィカルに作成します。 **受領書フォーマット デザイナー** ページには 3 つのセクションがあります。**ヘッダー**、**明細行**、および **フッター** です。 3 つのすべてのセクションの要素を使用するフォーム レイアウトもあれば、1 つまたは 2 つのセクションの要素しか使用しないフォーム レイアウトもあります。 各セクションで使用できる要素を表示するには、ページの左側のナビゲーション ウィンドウのボタンをクリックします。

1. **Retail とコマース** &gt; **チャネル設定** &gt; **POS 設定** &gt; **POS** &gt; **受領書フォーマット** をクリックします。
2. **受領書フォーマット** ページで、フォーム レイアウトを選択し、**デザイナー** をクリックします。
3. コマース デザイナー ホストのインストールを開始するには、**実行** をクリックします。
4. ワンクリック デザイナーのインストールを開始する場合、Internet Explorer ウィンドウの下部に表示される通知バーの **開始** をクリックします。 (通知バーは、他のブラウザの別の場所に表示されることがあります。) 進行状況インジケータは、インストール プロセスの進行状況を示します。
5. インストール完了後に、デザイナーを開始する場合、コマースのユーザー名とパスワードを入力し、**サインイン** をクリックします。
6. 資格情報を検証しデザイナーを開始した後に、受領書フォーマットを作成するか、または既存のフォーマットを変更することができます。
7. フォームの要素を作成するには、**ヘッダー**、**明細行**、または **フッター** セクションを選択し、セクションの要素をワークスペースにドラッグします。 ほとんどの要素は、データベースからデータが自動的に入力される変数で構成されます。 **テキスト** などのその他の要素は、カスタム テキストをレシートに印刷できます。

    > [!NOTE]
    > それぞれのセクションで使用する行数は、そのセクションの右下隅にある数値を調整することで選択できます。 セクションを変更しやすいように、セクション下部のサイズ変更バーをドラッグして、その高さを増やします。 ワークスペースのセクションの高さは、実際のレシートの行数に影響しません。

8. 要素をワークスペースにドラッグした後、ページ下部にある **オブジェクト情報** ウィンドウでパーツのプロパティを設定します。 次の 1 つまたは複数の設定を入力します。

    - **配置** – フィールドの配置を **左** または **右** に設定します。
    - **充填文字** - 空白文字を指定します。 既定では、空白を使用しますが、任意の文字を入力できます。
    - **接頭語** - フィールドの先頭に表示される値を入力します。 この設定は、レイアウトの **明細行** セクションにのみ適用されます。
    - **文字** – 要素に変数が含まれている場合に、フィールドに含めることができる文字の最大数を指定します。 フィールドのテキストが指定した文字数よりも長い場合は、フィールドに合わせて切り詰めます。
    - **変数** - 要素が変数を含むためにカスタマイズできない場合は、このチェック ボックスが自動的にオンになります。
    - **フォントの種類** - フォント スタイルを **通常** または **太字** に設定します。 太字の文字は、通常の文字の 2 倍のスペースを使用します。 したがって、一部の文字が切り詰められる場合があります。
    - **フォント サイズ** - フォント サイズを **通常** または **大** に設定します。 [大] の文字は [通常] の文字より 2 倍高くなります。 したがって、[大] の文字を使用すると、レシートでテキストが重なる可能性があります。
    - **削除** – 選択したパーツをフォーム レイアウトから削除する場合は、このボタンをクリックします。

## <a name="assign-receipt-profiles"></a>レシート プロファイルの割り当て

ハードウェア プロファイルを通じてレシート プロファイルがプリンタへ直接割り当てられます。

1. **Retail とコマース** &gt; **チャネル設定** &gt; **POS 設定** &gt; **POS プロファイル** &gt; **ハードウェア プロファイル** をクリックして、ハードウェア プロファイルを開きます。
2. 次に、プリンタを選択し、**レシート プロファイル** フィールドで、レジスターを使用してレシート プロファイルを割り当てます。

> [!NOTE]
> 2 つのプリンターを使用する場合、１ つ目のプリンターは標準の 40 列のサーマル レシートの印刷に使用できます。 2 番目のプリンタは、通常、詳細情報を要求する全ページのレシート タイプの印刷に使用されます。 これらのレシート タイプでは、顧客注文のレシートおよび顧客請求書が含まれます。


[!INCLUDE[footer-include](../includes/footer-banner.md)]
