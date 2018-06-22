---
title: "支払コネクタの配置"
description: "このトピックでは、支払コネクタ パッケージを適切なコンポーネントに配置する方法について説明します。"
author: aamirallaqaband
manager: AnnBe
ms.date: 01/12/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
audience: IT Pro
ms.reviewer: sericks
ms.search.scope: Operations, Retail
ms.custom: 141393
ms.assetid: e23e944c-15de-459d-bcc5-ea03615ebf4c
ms.search.region: Global
ms.search.industry: Retail
ms.author: aamiral
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 7.0.1
ms.translationtype: HT
ms.sourcegitcommit: 879eb9f2a63a8514791f74965005ed3e22bc0de7
ms.openlocfilehash: 1e291aa1437e4ec6d909428dc3a1176bb7781e56
ms.contentlocale: ja-jp
ms.lasthandoff: 04/20/2018

---

# <a name="deploy-a-payment-connector"></a>支払コネクタの配置

[!include [banner](../includes/banner.md)]

<a name="overview"></a>概要
--------

このトピックでガイドretail ITプロフェッショナルまたは支払コネクタを適切なコンポーネントに展開するプロセスを通じて付加価値再販業者 (Var)。このトピックでは、小売 IT プロフェッショナルまたは付加価値再販業者 (VARs) が支払コネクタを適切なコンポーネントに展開するプロセスについて説明します。 支払コネクタが支払プロバイダーまたは支払独立系ソフトウェア ベンダー (ISV) によって実装されてテスト済みであり、また顧客環境での検証とそれに続く実稼働配置の準備ができていると仮定します。 このトピックには、Retail ソフトウェア開発キット (SDK) を使用して支払コネクタをパッケージ化する方法に関する情報は含まれていません。 SDK をダウンロードする方法の詳細については、[Retail SDK 概要](retail-sdk/retail-sdk-overview.md)を参照してください。 支払コネクタをパッケージ化する方法の指針については、ダウンロードした SDK 内で、修正プログラム KB 3183058 の SDK で利用可能になった、支払コネクタを追加するの Retail SDK ハンドブック セクションを確認してください。 このトピックには、支払 Web アプリケーション、支払フロント エンド プロセッサ、またはバックエンド プロセッサの配置方法に関する情報も含まれています。それは、これらのアプリケーションが支払プロバイダーまたは支払 ISV によって管理されているためです。

## <a name="before-you-begin"></a>準備
支払プロバイダーまたは支払 ISV は、支払コネクタを作成します。 支払コネクターには、次のフォルダーの一部または全部が含まれます。

-   **IPaymentProcessor Assemblies** – このフォルダーには、IPaymentProcesor インターフェイスを実装するアセンブリとその依存アセンブリが含まれています。
-   **支払 Web ファイル** – このフォルダには、支払受け入れページを有効にするために必要なコールバック HTML、JavaScript、または CSS ファイルが含まれています。 支払い受付ページで求められる場合、支払コネクタ開発者がこれらの Web ファイルを提供します。
-   **IPaymentDevice Assemblies** – このフォルダーには、IPaymentDevice インターフェイスを実装するアセンブリとその依存アセンブリが含まれています。 これらのアセンブリは、VeriFone MX925 などの決済端末デバイスと通信するために、Retail ハードウェア ステーションおよび Retail Modern 販売時点管理 (Modern POS) で使用されます。 支払のターミナル デバイスがない場合は、これらのファイルは必要ありません。

支払プロバイダまたは支払 ISV が提供する支払コネクタ ファイルをパッケージ化するには、Retail SDK の修正プログラム KB 3183058 (またはそれ以降) を使用する必要があります。 Retail SDK をビルドした後は、次の展開可能なパッケージを入手します。

-   Application Object Server (AOS) 支払パッケージ
-   配置可能小売パッケージ

開始する前に、次の品目が必要です。

-   支払コネクタ ファイル
-   Retail SDK 用 KB 3183058
-   Retail SDK を使用して作成された展開可能パッケージ (このトピックの前のリストを参照)
-   Microsoft Dynamics Lifecycle Service (LCS) のクラウド ホスト環境へのアクセス

## <a name="deployable-packages-automated-deployment"></a>配置可能パッケージ (自動展開)
デプロイ可能なパッケージは、LCS デプロイメント サービスで利用可能なアセットです。 支払コネクタを配置可能なパッケージとして作成するときは、支払コネクタを既存のソリューションにカスタマイズとしてインストールすることが、または新しい配置の一部としてスリップ ストリームすることができます。 次のタイプのパッケージには、支払コネクタが含まれています。

-   **AOSPaymentPackage** - このタイプのパッケージは、AOS に 1 つ以上の支払コネクタを配置します。
-   **RetailDeployablePackage** – このタイプのパッケージは、以下のコンポーネントに 1 つまたは複数の支払いコネクタを配置します。    -   Retail サーバー
    -   クラウド POS
    -   次のインストールを可能にするセルフ サービス インストーラー:
        -   ハードウェア ステーション
        -   Modern POS

### <a name="upload-and-deploy-deployable-packages"></a>展開可能なパッケージのアップロードと展開

1.  LCS プロジェクト ページを開きます。
2.  **追加ツール** セクションで、**アセット ライブラリ**をクリックします。
3.  **ソフトウェア パッケージ** を選択し、プラス記号をクリックします (**+**)。
4.  名前と説明を入力し、次の表に示すように、適切なパッケージ タイプを選択します。

    | 配置可能パッケージ      | LCS の配置可能パッケージ タイプ |
    |-------------------------|--------------------------------|
    | AOSPaymentPackage       | バイナリ修正プログラム                  |
    | RetailDeployablePackage | 結合された小売パッケージ        |

5.  **アップロード** をクリックします。
6.  圧縮済みのパッケージを選択してアップロードし、**確定** をクリックします。

配置可能パッケージを LCS 資産ライブラリにアップロードした後、LCS ポータルを通じて環境に配置することができます。 サンドボックス環境内の配置を検証した後は、実稼働環境を配置するサービス要求を作成できます。 詳細については、[配置可能パッケージの適用](../../dev-itpro/deployment/apply-deployable-package-system.md) を参照してください。

#### <a name="download-and-run-installers-on-client-computers"></a>クライアント コンピューターでインストーラーをダウンロードして実行

セルフサービス パッケージには、ハードウェア ステーションと Modern POS の両方のインストーラーが含まれています。 配置可能パッケージが環境に適用された後、更新されたハードウェア ステーションと Modern POS インストーラーをダウンロードすることができます。 ハードウェア ステーションおよび Modern POS をダウンロードし、クライアント コンピューターにインストールする方法の詳細については、[Retail Modern POS セルフ サービス ダウンロードとインストール、および Modern POS とクラウド POS のデバイスの有効化](../retail-modern-pos-device-activation.md) を参照してください。

## <a name="manual-deployment"></a>手動での配置
このセクションでは、支払コネクタを手動で展開する方法について説明します。 手動による展開を使用して、開発環境でローカルにテストすることができます。 この開発環境は、クラウドホスト型でも、ダウンロード可能な仮想ハード ディスク (VHD) 上でも構いません。

### <a name="put-the-payment-connector-assemblies-and-files-in-the-correct-locations"></a>支払コネクタ アセンブリとファイルを正しい場所に配置

支払コネクタはプラグ可能です。 開発環境では、サーバーの適切な場所に適切なファイルを配置できます。 次のテーブルは、どのファイルをどの場所に置くべきかを示しています。

|                                                                            | IPaymentProcessor Assemblies フォルダーのコンテンツ                       | 支払い Web ファイル フォルダーのコンテンツ | IPaymentDevice Assemblies フォルダーのコンテンツ |
|----------------------------------------------------------------------------|---------------------------------------------------------------------------|------------------------------------------|--------------------------------------------------|
| Application Object Server (AOS)                                            | &lt;*Aos.PackageDirectory*&gt;/bin/Connectors/ &lt;*Aos.WebRoot*&gt;/bin/ | &lt;*Aos.WebRoot*&gt;/Connectors/        | 該当なし                                   |
| Retail サーバー                                                              | &lt;*RS.WebRoot*&gt;/bin/                                                 | 該当なし                           | 該当なし                                   |
| クラウド POS                                                                  | 該当なし                                                            | &lt;*CPOS.WebRoot*&gt;/Connectors/       | 該当なし                                   |
| リモート ハードウェア ステーション (インターネット インフォメーション サービス \[IIS\])            | &lt;*HWS.WebRoot*&gt;/bin/                                                | 該当なし                           | &lt;*HWS.WebRoot*&gt;/bin/                       |
| Modern POS のローカルのハード ステーション (情報の保護とコントロール \[IPC\]) | &lt;*MPOS.AppRoot*&gt;/ClientBroker/                                      | 該当なし                           | &lt;*MPOS.AppRoot*&gt;/ClientBroker/             |
| E コマース                                                                 | 該当なし                                                            | &lt;*ECOM.WebRoot*&gt;/Connectors/       | 該当なし                                   |

上記のテーブルへのキーを次に示します。

-   &lt;*Aos.PackageDirectory*&gt; は AOS のパッケージ ディレクトリです。 パスは AOS の web.config ファイルから見つけることができます (key = **Aos.PackageDirectory**)。
-   &lt;*Aos.WebRoot*&gt; は AOS の Web アプリケーション ルートです。
-   &lt;*RS.WebRoot*&gt; は Retail サーバーの Web アプリケーション ルートです。
-   &lt;*HWS.WebRoot*&gt; はリモート ハードウェア ステーションの Web アプリケーション ルートです。
-   &lt;*MPOS.AppRoot*&gt; は Modern POS (例えば、C:\\Program Files (x86)\\Microsoft Dynamics AX70\\Retail Modern POS など) のアプリ インストール フォルダーです。
-   &lt;*ECOM.WebRoot*&gt; は電子商取引 Web サイト の Web アプリケーション ルートです。

支払 Web ファイル フォルダーには通常、サブフォルダーが含まれます。 サブフォルダー全体をターゲットの場所にコピーしてください。

## <a name="use-a-payment-connector-with-an-ecommerce-site"></a>電子商取引サイトで支払コネクタを使用
E コマース サイトは、LCS の管理された環境では配置されていません。 パートナーと連携して、電子商取引サイトをホストする方法を決定する必要があります。 支払コネクタに支払 Web ファイルが必要とされる場合は、電子商取引にこれらの Web ファイルを配置する必要があります。 支払コネクタが、支払 Web ファイルを必要としない場合、追加の手順は必要ありません。 Web ファイルの支払を電子商取引サイトに配置する方法については、記事の前半の「支払コネクタ アセンブリおよびファイルを正しい場所に配置する」セクションを参照してください。

<a name="additional-resources"></a>その他のリソース
--------

[支払コネクタと支払デバイスの実装ガイド](http://download.microsoft.com/download/4/D/7/4D7C6B05-0C23-4C6C-BA13-AB62ED08AA61/The%20Guide%20to%20Implementing%20Payment%20Connector%20and%20Payment%20Device.docx)

[Retail SDK 小売パッケージ](retail-sdk/retail-sdk-packaging.md)




