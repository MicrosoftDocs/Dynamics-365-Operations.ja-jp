---
title: 地域の検出とリダイレクトを設定する
description: この記事では、Microsoft Dynamics 365 Commerce での eコマース サイトの地域検出とリダイレクトの設定方法について説明します。
author: bicyclingfool
ms.date: 04/06/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: shajain
ms.search.validFrom: ''
ms.custom: ''
ms.assetid: ''
ms.search.industry: Retail
ms.openlocfilehash: e8f65d1243c43de8df23d7cb6ec3207fbdfff8fb
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/12/2022
ms.locfileid: "9287608"
---
# <a name="set-up-geo-detection-and-redirection"></a>地域の検出とリダイレクトを設定する

[!include [banner](../includes/banner.md)]

この記事では、Microsoft Dynamics 365 Commerce での eコマース サイトの地域検出とリダイレクトの設定方法について説明します。

Dynamics 365 Commerce によって、特定の国や地域に適した購買やショッピング エクスペリエンスを作成できます。 たとえば、特定の国や地域の e コマース エクスペリエンスの製品、品揃え、カテゴリ、価格、フルフィルメント、などさまざまな側面を定義できます。 

Dynamics 365 Commerce の地域検出およびリダイレクト機能を使用すると、顧客の地理的位置を検出し、その情報を使用して、各顧客が住んでいる国または地域に最も適したサイトを推奨できます。 

現住所の国または地域に関連付けされていないサイト URL を要求する顧客向けに、2 つのエクスペリエンスのいずれかを選択できます。

- [国/地域の選択](country-region-picker-module.md)を使用して、顧客に自分の場所に関連付けられている 1 つまたは複数のサイトを選択するように促すか、最初に要求したサイトに進むかを選択するよう求めます。
- 顧客は、その国または地域に関連付けられているサイトに自動的にリダイレクトされます。

たとえば、カナダの顧客が、カナダに関連付けされていないサイトを要求したとします。 この場合、国/地域の選択モジュールには、カナダ向けに設定されているサイトをリストしたダイアログ ボックスが表示されます。 次の図の例では、カナダ向けの英語およびフランス語のサイトのオプションがダイアログ ボックスに含まれています。

![カナダ向けの英語およびフランス語のサイトについてのオプションを示す地域/言語選択ダイアログ ボックスの例。](./media/Geo_Country-region-picker.png)

顧客がオプションを選択すると、そのサイトにリダイレクトされます。 または、地域の自動リダイレクトが有効になっている場合、顧客はオンライン チャネルの既定のロケールとしてマークされているロケールに自動的にリダイレクトされます。 

顧客のサイト基本設定は、Cookie にもキャプチャされます。 これにより、顧客が次にそのサイトにアクセスした時に、サイトを選択するように求められることはありません。 代わりに、自動的に優先サイトにリダイレクトされます。

## <a name="enable-geo-redirection-features-in-commerce-site-builder"></a>Commerce サイト ビルダーの地域リダイレクト機能の有効化

Commerce サイト ビルダーのサイトで地域リダイレクトを有効にするには、**サイト設定 \> 一般** に移動し、**地域リダイレクト機能の有効化** 設定をオンにします。

> [!IMPORTANT]
> **地域リダイレクト機能の有効化** 設定をオンにする前に、**場所に基づく店舗検出の有効化** 設定をオンにします。 詳細については、[場所に基づく店舗検出の有効化](enable-store-detection.md)を参照してください。

## <a name="initialize-the-commerce-scheduler"></a>Commerce スケジューラの初期化

Commerce 本部に入力する国/地域データの同期を有効にするには、**Retail と Commerce \> バックオフィス設定 \> Commerce スケジューラ \> Commerce スケジューラの初期化** で、Commerce スケジューラを初期化する必要があります。 Commerce スケジューラの詳細については、[コンフィギュレーションの更新](dev-itpro/cdx-best-practices.md#update-configurations)を参照してください。 

> [!NOTE]
> Commerce バージョン 10.0.24 リリース以降、Commerce スケジューラは Commerce 本部の更新後に自動的に実行するように設定できます。 Commerce 本部でこの機能を有効にするには、**ワークスペース \> 機能管理** に移動し、**本部の機能が更新された後に "Commerce スケジューラの初期化" を実行** する機能を有効にしてください。 

## <a name="associate-countries-and-regions-with-online-stores-in-commerce-headquarters"></a>Commerce 本社でのオンライン ストアへの国と地域の関連付け

国と地域は、Commerce 本社のオンライン ストア (オンライン チャネルとも呼ばれる) に関連付けられています。 国または地域をオンライン ストアに関連付ける場合は、その国または地域に居住する顧客が、そのオンライン ストアにマップされているサイトを表示する必要があることを示します。 必要に応じて、複数の国や地域をオンライン ストアに関連付けることができます。

国または地域をオンライン ストアに関連付けるには、次の手順を実行します。

1. **Retail と Commerce \> チャネル \> オンライン ストア** に移動するか、検索ボックスで "オンライン ストア" を検索します。
1. 国または地域と関連付けるオンライン チャネルを開きます。
1. **国/地域** クイック タブで **追加** を選択し、**国/地域** フィールドで、国または地域を選択します。
1. オンライン チャネルに関連付ける他の国または地域に対して、上の手順を繰り返します。

![Commerce 本社でオンライン ストアにマップされている国や地域を示す例。](./media/Geo_HQ-Country-Mapping.png)

国や地域のオンライン ストアへの関連付けが完了したら、**Retail および Commerce \> Retail および Commerce IT** に移動し、**配送スケジュール** ビューで、ジョブ 1070 (**チャネル コンフィギュレーション**) を実行してください。 そのジョブが完了すると、オンライン ストアに関連付けた国と地域が、Commerce サイト ビルダーの **サイト設定** にある **チャネル** ページで利用できるようになります。

## <a name="configure-geo-redirection-rules-in-commerce-site-builder"></a>Commerce サイト ビルダーの地域リダイレクト ルールのコンフィギュレーション

チャネル構成ジョブが完了すると、国/地域を **サイト設定** にある **チャネル** ページで定義したサイト URL にマップできます。 国/地域をサイト URL にマップすると、その国/地域に住んでいる顧客が、居住する国/地域にマップされていない URL を要求する場合に、そのサイト URL を提供する必要があることを申告していることになります。 

国/地域は、異なるチャネルまたは同じチャネルのいずれかに関連付けられている URL にマップできます。 製品、品揃え、価格決定、割引、支払方法、配送モードなど、小売 e コマース エクスペリエンスのその他の側面は、チャネル レベルでカスタマイズされます。 ただし、同じチャネル内で e コマース サイトのいくつかの側面をロケールで区別することもできます。 <!--To learn more about options and the scenarios they enable, see [Channel mapping to e-commerce sites](channel-mapping-to-ecom-site.md).--> 

### <a name="associate-countries-and-regions-with-urls"></a>国と地域を URL に関連付ける

国および地域をサイト URL に関連付けるには、次の手順を実行します。

1. Commerce サイト ビルダーで、**サイト設定 \> チャネル** に移動します。
1. チャネル名を選択し、ロケールを選択します。
1. 選択したチャネルとロケールの組み合わせに対応する URL に関連付ける 1 つ以上の国または地域を選択します。
1.  **OK** を選択します。
1. **保存して公開** を選択して変更を保存し、公開します。

### <a name="enable-automatic-redirection"></a>自動リダイレクトを有効にする

国/地域の選択ダイアログ ボックスから URL を選択するように顧客に求める代わりに、特定の国または地域の顧客を指定した URL に自動的にリダイレクトすることができます。 たとえば、日本に住んでいる顧客が、日本のチャネルと言語にマップされたサイトに自動的に送られるようにするとします。 その場合、URL がコンフィギュレーションされているチャネルで **自動リダイレクト** 設定をオンにします。 変更を保存して公開すると、日本の顧客はその URL に自動的に送られ、国/地域の選択ダイアログ ボックスは表示されません。

国または地域に複数の URL を関連付けることができます。 この場合、自動リダイレクトはチャネルの既定ロケールとして指定されたロケールの URL を使用します。

### <a name="geo-detection-and-redirection-logic"></a>地域検出およびリダイレクトのロジック

Dynamics 365 Commerce の地域検出およびリダイレクトは、顧客の国または地域を Commerce サイト ビルダーの **チャネル** ページの URL にマップされている国および地域のリストと比較することによって機能します。

顧客がサイトの URL を要求すると、システム リダイレクト ロジックは、顧客の国または地域が要求された URL にマップされているかどうかを判断します。 マップされている場合は、顧客は引き続きその URL を使用します。 そうでない場合は、リダイレクト ロジックは顧客の国や地域にマップされている URL を検索して、その URL を推奨 URL として顧客に示します。 顧客の国または地域に対して自動リダイレクトが有効になっている場合、顧客は自動的に、その国または地域の最適な URL にリダイレクトされます。 自動リダイレクトにどの URL を使用するかを定義する方法の詳細については、[自動リダイレクトのコンフィギュレーション](#enable-automatic-redirection)を参照してください。

次のワークフロー図は、リダイレクト ロジックの手順と決定事項を示しています。

![リダイレクト ロジックの手順と決定事項を示すワークフロー図。](./media/Geo_Redirection-Logic.png)

## <a name="configure-the-countryregion-picker-module"></a>国/地域の選択モジュールのコンフィギュレーション

Commerce モジュール ライブラリに含まれている国/地域の選択モジュールは、国または地域に関連付けられていない URL を要求する顧客に推奨 URL を表示します。 国/地域の選択モジュールのコンフィギュレーションの詳細については、[国/地域の選択モジュール](country-region-picker-module.md)を参照してください。

## <a name="save-customer-site-preferences"></a>顧客サイトの基本設定の保存

Commerce サイト ビルダーで **地域リダイレクト機能の有効化** 設定がオンになっている場合、地域リダイレクトは顧客のサイト基本設定を保存します。 国/地域の選択ダイアログ ボックスで推奨 URL を選択した顧客がそのサイトに移動する前に、選択した URL は、顧客が現在いるドメインの **\_msdyn365\_\_\_site\_** Cookie に書き込まれます。 次に、顧客が以前に国/地域の選択ダイアログ ボックスを表示する元となった URL を要求すると、顧客は自動的に優先サイトにリダイレクトされます。

### <a name="site-selector-module"></a>サイト セレクター モジュール

顧客がサイトを **\_msdyn365\_\_\_site\_** Cookie に書き込ませるアクションを実行すると、そのサイトに自動的にリダイレクトされます。 ほとんどの場合、この動作によって、顧客の国または地域に適した e コマース エクスペリエンスが生成されます。 ただし、一部の顧客は、別の国/地域固有のサイトを選択したいか、または選択する必要があるるかもしれません。 それで、顧客が自動リダイレクトを上書きできるように、サイトで[サイト セレクタ モジュール](site-selector.md)を使用することもお勧めします。 サイト セレクタ モジュールは、国/地域の選択と同じ国/地域を、関連付けられているサイトの URL と共に表示するように構成できます。 顧客がサイト セレクターを使用して別の国/地域固有のサイトを選択すると、モジュールは顧客のサイト設定で **\_msdyn365\_\_\_site\_** Cookie も更新します。 次回顧客がアクセスする時、国/地域の選択で、その設定が優先されます。 

## <a name="additional-resources"></a>追加リソース

[サイト セレクター モジュール](site-selector.md)

[場所に基づく店舗検出の有効化](enable-store-detection.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
