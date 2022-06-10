---
title: Customer Voice を e コマース サイト ページに統合する
description: このトピックでは、Microsoft Dynamics 365 Customer Voice を Dynamics 365 Commerce の eコマース サイトに統合する方法について説明します。
author: samjarawan
ms.date: 05/17/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: samjar
ms.search.validFrom: 2019-10-31
ms.openlocfilehash: 272ec1a59ed45b2d2336dcfea16051d27011360f
ms.sourcegitcommit: 48d094d083c1bd45c3d72f8b666926b48ec7ae35
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/18/2022
ms.locfileid: "8767954"
---
# <a name="integrate-customer-voice-into-e-commerce-site-pages"></a>Customer Voice を e コマース サイト ページに統合する

[!include [banner](../includes/banner.md)]

このトピックでは、Microsoft Dynamics 365 Customer Voice を Dynamics 365 Commerce の eコマース サイトに統合する方法について説明します。

[Customer Voice](https://dynamics.microsoft.com/customer-voice/overview/) を e コマース サイトに統合して、リアルタイムの顧客フィードバックを収集、分析、追跡できます。 統合を開始するには、アカウントを作成して、収集するフィードバックのタイプとして Customer Voice プロジェクト テンプレートを選択する必要があります。

## <a name="integrate-the-customer-voice-service"></a>Customer Voice サービスの統合

Customer Voice アカウントを作成するには、[Customer Voice](https://dynamics.microsoft.com/customer-voice/overview/) に移動し、メッセージに従います。

Customer Voice アカウントを作成してサインインした後、次のステップは収集するフィードバックのタイプとしてプロジェクト テンプレートを選択する必要があります。

Customer Voice テンプレートを選択するには、次の手順に従います。

1. [Customer Voice テンプレート ページ](https://customervoice.microsoft.com/Pages/ProjectPage.aspx) に移動します。
1. **開始する** を選択します。
1. 収集するフィードバックの種類に大してプロジェクト テンプレートを選択して、**次へ** を選択します。
1. **送信** タブの **埋め込み形式を選択** で、埋め込み形式を選択します。 **埋め込みコード** フィールドには、Commerce サイト ビルダに埋め込む必要があるコードが表示されます。

このトピックの例では、**定期処理顧客アンケート** プロジェクト テンプレートと **ボタン** 埋め込み形式を使用します。

次の例は、**定期処理顧客アンケート** プロジェクト テンプレート ページで、**ボタン** の埋め込み形式のオプションが選択され、そのオプションの埋め込みコードが **埋め込みコード** フィールドに表示される場合の例です。 次のセクションで説明するように、指定したコードをサイト ページに埋め込むには、3 つの別々のアクションが必要です。

![[ボタン] オプションが選択された Customer Voice Periodic 顧客アンケートページ。](media/customer-voice-integration-1.png)

### <a name="embed-the-external-script-url"></a>外部スクリプト URL の埋め込み

Customer Voice アンケートが必要なすべてのサイト ページに、Customer Voice が埋め込みコードで提供した外部スクリプト URL を埋め込む必要があります。 複数のサイト ページにスクリプトを埋め込むには、外部スクリプト URL を含む片をサイト ビルダに作成し、その片を適切なページ テンプレートに追加する方法が最善の方法です。 更新されたテンプレートを公開すると、影響を受けるサイト ページで埋め込み外部スクリプト コードが次の例のようになります。

```html
<script src=https://mfpembedcdnmsit.azureedge.net/mfpembedcontmsit/Embed.js type="text/javascript"></script>
```

フラグメントの詳細については、[フラグメントを使って作業する](work-with-fragments.md) を参照してください。

> [!NOTE]
> 必要な URL をフラグメントに追加します。 外部スクリプト モジュールに、その他のスクリプト コードが追加されます。

外部スクリプト URL をフラグメントに埋め込むには、次の手順に従います。

1. サイト ビルダーで、[外部スクリプト モジュール](script-module.md) に基づくフラグメントを作成します。
1. 新規フラグメントで、**既定の外部スクリプト** スロットを選択します。
1. **スクリプト ソース** で **既定の外部スクリプト** プロパティ ウィンドウで、次の例の図にある通り、外部スクリプト URL を入力します。

    ![新規フラグメントのスクリプト ソース フィールドにあるスクリプト URL。](media/customer-voice-integration-2.png)

1. **保存** を選択し、**編集完了** を選択します。
1. **公開** を選択して、フラグメントを公開します。

埋め込み外部スクリプト ブロックを含む新しい片を適切なページ テンプレートに追加する準備が整いました。

### <a name="embed-the-external-style-sheet-code"></a>外部スタイル シート コードの埋め込み

次に、Customer Voice アンケートを持つべきすべてのサイト ページで、Customer Voice が埋め込みコードで提供された外部スタイルシート コードを埋め込む必要があります。 前セクションで述べた通り、複数のサイト ページに外部スタイルシート コードを埋め込むには、スタイルシート コードを含む片をサイト ビルダーでフラグメントを作成し、そのフラグメントを適切なページ テンプレートに追加する方法が最善の方法です。 埋め込み外部スタイル シート コードは、次のコード例のようになります。

```typescript
<link rel="stylesheet" type="text/css" href=https://mfpembedcdnmsit.azureedge.net/mfpembedcontmsit/Embed.css />
```

外部スタイルシート コードをフラグメントに埋め込むには、次の手順に従います。

1. サイト ビルダーで、[メタタグ モジュール](metatags-module.md) に基づくフラグメントを作成します。
1. フラグメントで、**既定のメタタグ** スロットを選択し ます。
1. **既定のメタタグ** プロパティ ウィンドウで、**メタタグ** フィールドで、次の例の図にある通り、スタイルシート コードを入力します。

    ![新しいフラグメントに対する、メタタグ フィールドの外部スタイル シート コード。](media/customer-voice-integration-3.png)

1. **保存** を選択し、**編集完了** を選択します。
1. **公開** を選択して、フラグメントを公開します。

埋め込み外部スタイルシート コードを含む新しいフラグメントを適切なページ テンプレートに追加する準備が整いました。

### <a name="embed-the-inline-script-code"></a>埋め込みインライン スクリプト コード 

次に、Customer Voice アンケートを持つべきすべてのサイト ページで、Customer Voice が埋め込みコードで提供されたインライン スクリプト コードを埋め込む必要があります。 前セクションで述べた通り、複数のサイト ページにインライン スクリプト コードを埋め込むには、インライン スクリプト コードを含むサイト ビルダーでフラグメントを作成し、そのフラグメントを適切なページ テンプレートに追加する方法が最善の方法です。

次の例では、インライン スクリプト コードの例では、**SURVEY\_KEY** がプレースホルダーです。 **SURVEY\_KEY** の値は、埋め込みコードにCustomer Voice が提供した実際のアンケートキーと一致する必要があります。 最後の行は、スクリプトの読み込み時間を確保するために、コードを 1 秒後に表示するためにコードを呼び出します。 選択したアンケートによっては、会社名などの他のメタデータを追加または更新する必要がある場合があります。

```html
function renderSurveyButton() {
    var se = new SurveyEmbed("SURVEY_KEY","https://customervoice.microsoft.com/","https://mfpembedcdnmsit.azureedge.net/mfpembedcontmsit/","true");

    var context = {
        "First Name":"",
        "Last Name": "",
        "locale": "en-us",
        "companyname": "Adventure Works"
    };
    se.renderButton(context);
}

setTimeout(renderSurveyButton, 4000);
```

インライン スクリプト コードをフラグメントに埋め込むには、次の手順に従います。

1. サイト ビルダーで、[インライン スクリプト モジュール](script-module.md) に基づくフラグメントを作成します。
1. 新規フラグメントで、**既定のインライン スクリプト** スロットを選択します。
1. **既定のインライン スクリプト** プロパティ ウィンドウで、**インライン スクリプト** フィールドプロパティ ウィンドウで、次の例の図にある通り、インライン スクリプト コードを入力します。

    ![新規フラグメントのインライン スクリプト フィールドにあるインライン スクリプト コード。](media/customer-voice-integration-4.png)

1. **保存** を選択し、**編集完了** を選択します。
1. **公開** を選択して、フラグメントを公開します。

埋め込みインライン スクリプト コードを含む新しいフラグメントを、適切なページ テンプレートに追加する準備が整いました。

## <a name="add-fragments-to-a-template"></a>フラグメントをテンプレートに追加する

Customer Voice 埋め込みコードを含むフラグメントの作成が完了したら、それらを使用するサイト ページに関連付けられているページ テンプレートに追加する必要があります。 次の例の図では、3 つの例のフラグメントが製品の詳細ページ (PDP) テンプレートに追加されています。

![PDP テンプレートに追加するフラグメント例。](media/customer-voice-integration-5.png)

更新したテンプレートの公開後は、Customer Voice アンケートがテンプレートによって制御されるすべてのページに表示されます。

テンプレートの詳細については、[テンプレートを使って作業する](work-with-templates.md) を参照してください。

## <a name="configure-content-security-policy"></a>コンテンツ セキュリティ ポリシーを構成する

既定では、コンテンツ セキュリティ ポリシー (CSP) では、追加の構成が行われない限り、他のサービスへの呼び出しは許可されません。 したがって、更新したテンプレートを公開すると、関連するサイト ページにアンケートが読み込まれそうにありません。 何も表示されていない場合は、Web ブラウザの開発者ツール (F12) を開き、アンケートを行っているページに移動します。 コンソール出力には、CSP 関連のエラーが表示されます。

エラーを修正するためにサイトで CSP を構成するには、次の手順に従います。

1. **サイト 設定 \> 拡張** に移動します。
1. **コンテンツ セキュリティ ポリシー** タブで、`https://customervoice.microsoft.com/` を **child-src** ディレクティブに追加します。
1. `https://customervoice.microsoft.com/` を **frame-src** に追加します。
1. `https://mfpembedcdnmsit.azureedge.net` と **.azureedge.net** を **img-src** ディレクティブに追加します。

詳細については、[コンテンツ セキュリティ ポリシー](manage-csp.md)を参照してください。

## <a name="additional-resources"></a>追加リソース

[外部スクリプト モジュール](script-module.md)

[メタタグ モジュール](metatags-module.md)

[インライン スクリプト モジュール](script-module.md)

[コンテンツ セキュリティ ポリシー](manage-csp.md)

[フラグメントで動作](work-with-fragments.md)

[テンプレートの使用](work-with-templates.md)
