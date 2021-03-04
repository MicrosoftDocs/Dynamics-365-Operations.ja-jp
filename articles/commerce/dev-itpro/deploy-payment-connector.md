---
title: 支払コネクタの配置
description: このトピックでは、支払コネクタ パッケージを適切なコンポーネントに配置する方法について説明します。
author: aamirallaqaband
manager: AnnBe
ms.date: 05/07/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: IT Pro
ms.reviewer: rhaertle
ms.custom: 141393
ms.assetid: e23e944c-15de-459d-bcc5-ea03615ebf4c
ms.search.region: Global
ms.search.industry: Retail
ms.author: aamiral
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 7.0.1
ms.openlocfilehash: 6650f179038484f19f6f9f265b526213f65c7032
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 12/05/2020
ms.locfileid: "4684979"
---
# <a name="deploy-payment-connectors"></a>支払コネクタの配置

[!include [banner](../includes/banner.md)]

## <a name="overview"></a>概要

このトピックでは、IT プロフェッショナルまたは付加価値再販業者 (VAR) が支払コネクタを適切なコンポーネントに展開するプロセスについて説明します。 支払コネクタが支払プロバイダーまたは支払独立系ソフトウェア ベンダー (ISV) によって実装されてテスト済みであり、また顧客環境での検証とそれに続く実稼働配置の準備ができていると仮定します。

このトピックには、Retail ソフトウェア開発キット (SDK) を使用して支払コネクタをパッケージ化する方法に関する情報は含まれていません。 SDK のダウンロード方法に関する詳細は、 [Retail ソフトウエア開発キット (SDK) アーキテクチャ](retail-sdk/retail-sdk-overview.md) を参照してください。 支払コネクタをパッケージ化する方法のガイドラインについては、ダウンロードした SDK の Retail SDK パッケージ ドキュメントを参照してください。

このトピックには、支払 Web アプリケーション、支払フロントエンド プロセッサ、または支払バックエンド プロセッサの配置方法に関する情報も含まれています。それは、これらのアプリケーションが支払プロバイダーまたは支払 ISV によって管理されているためです。 Microsoft Dynamics AX 7.0 (2016 年 2 月) を使用している場合は、コマース配置可能パッケージを作成する前に KB 3183058 を適用する必要があります。

## <a name="payment-packaging-folder"></a>支払パッケージ フォルダ

支払プロバイダーまたは支払 ISV は、支払コネクタを作成します。 支払コネクターには、次のフォルダーの一部または全部が含まれます。

> [!NOTE]
> これらのフォルダーは \\RetailSDK\\PaymentExternals で検索することができます。

- **IPaymentProcessor Assemblies** – このフォルダーには、IPaymentProcessor インターフェイスを実装するアセンブリとその依存アセンブリが含まれています。
- **支払 Web ファイル** – このフォルダには、支払受け入れページを有効にするために必要なコールバック HTML、JavaScript、または CSS ファイルが含まれています。 支払い受付ページで求められる場合、支払コネクタ開発者がこれらの Web ファイルを提供します。
- **IPaymentDevice Assemblies** – このフォルダーには、IPaymentDevice インターフェイスを実装するアセンブリと支払要求ハンドラー、およびインターフェイス依存アセンブリが含まれています。 これらのアセンブリは、VeriFone MX925 などの決済端末デバイスと通信するために、ハードウェア ステーションおよび Modern 販売時点管理 (Modern POS) で使用されます。 支払のターミナル デバイスがない場合は、これらのファイルは必要ありません。

支払コネクタ ファイルをパッケージ化するには、\\RetailSDK\\ PaymentExternals のフォルダへ支払アセンブリをコピーする必要があります。 支払アセンブリがコピーされた後、Retail SDK フォルダーのルートから **msbuild** を使用し、配置可能なパッケージを生成します。 **msbuild** 操作が完了した後、\\RetailSDK\\Packages\\ RetailDeployablePackage で配置可能パッケージを検索できます。

- **配置可能小売パッケージ** – このパッケージには、支払およびその他のすべてのチャネル拡張コンポーネントが含まれています。 これは、すべての拡張コンポーネントの結合されたパッケージです。 RetailDeployablePackage には、次のコンポーネントの支払コネクタが含まれています。
    
    - Commerce Scale Unit (CSU)
    - 次のインストールを可能にするセルフ サービス インストーラー:
        - Hardware station
        - Modern POS
        - Commerce Scale Unit (自己ホスト)

> [!NOTE]
> 10.0.10 以前のリリースでは、AOS および CSU の両方に RetailDeployablePackage を配置できます。 その後のリリースでは、RetailDeployablePackage は CSU にのみ配置できます。 支払コネクタを AOS アプリケーション バージョン 10.0.10 以降に配置するには、[セルフサービス配置のアプリケーション エクスプローラー用支払パッケージの作成](https://docs.microsoft.com/dynamics365/commerce/dev-itpro/payment-connector-package) の情報に従ってください。

### <a name="upload-and-deploy-deployable-packages"></a>展開可能なパッケージのアップロードと展開

1. LCS プロジェクト ページを開きます。
2. **追加ツール** セクションで、**アセット ライブラリ** をクリックします。
3. **ソフトウェア パッケージ** を選択し、プラス記号をクリックします (**+**)。
4. 名前と説明を入力し、次の表に示すように、適切なパッケージ タイプを選択します。

    | 配置可能パッケージ                    | LCS の配置可能パッケージ タイプ |
    |---------------------------------------|--------------------------------|
    | RetailDeployablePackage.zip               | 結合されたコマース パッケージ      |

5. **アップロード** をクリックします。
6. 圧縮済みのパッケージを選択してアップロードし、**確定** をクリックします。

配置可能パッケージを LCS 資産ライブラリにアップロードした後、LCS ポータルを通じて環境に配置することができます。 サンドボックス環境内の配置を検証した後は、実稼働環境を配置するサービス要求を作成できます。 詳細については、[配置可能パッケージの適用](../../dev-itpro/deployment/apply-deployable-package-system.md) を参照してください。

#### <a name="download-and-run-installers-on-client-computers"></a>クライアント コンピューターでインストーラーをダウンロードして実行

セルフサービス パッケージには、ハードウェア ステーションと Modern POS の両方のインストーラーが含まれています。 配置可能パッケージが環境に適用された後、更新されたハードウェア ステーションと Modern POS インストーラーをダウンロードすることができます。 ハードウェア ステーションおよび Modern POS をダウンロードし、クライアント コンピューターにインストールする方法については、[Modern POS (MPOS) のコンフィギュレーション、インストール、および有効化](../retail-modern-pos-device-activation.md) を参照してください。

## <a name="manual-deployment"></a>手動での配置

このセクションでは、支払コネクタを手動で展開する方法について説明します。 手動による展開を使用して、開発環境でローカルにテストすることができます。 この開発環境は、クラウドホスト型でも、ダウンロード可能な仮想ハード ディスク (VHD) 上でも構いません。 これらの手順は、サンドボックスまたは実稼動環境には適用されません。

### <a name="put-the-payment-connector-assemblies-and-files-in-the-correct-locations"></a>支払コネクタ アセンブリとファイルを正しい場所に配置

支払コネクタはプラグ可能です。 開発環境では、サーバーの適切な場所に適切なファイルを配置できます。 次のテーブルは、どのファイルをどの場所に置くべきかを示しています。

|  コネクタ | IPaymentProcessor Assemblies フォルダーのコンテンツ | 支払い Web ファイル フォルダーのコンテンツ | IPaymentDevice Assemblies フォルダーのコンテンツ |
|-----------|-----------------------------|------------------------------|---|
| Application Object Server (AOS)                                            | &lt;*Aos.PackageDirectory*&gt;/bin/Connectors/ &lt;*Aos.WebRoot*&gt;/bin/ | &lt;*Aos.WebRoot*&gt;/Connectors/        | 適用できません                                   |
| コマース スケール ユニット                                                              | &lt;*RS.WebRoot*&gt;/bin/                                                 | 適用できません                           | 適用できません                                   |
| クラウド POS                                                                  | 適用できません                                                            | &lt;*CPOS.WebRoot*&gt;/Connectors/       | 該当なし                                   |
| リモート ハードウェア ステーション (インターネット インフォメーション サービス \[IIS\])            | &lt;*HWS.WebRoot*&gt;/bin/                                                | 該当なし                           | &lt;*HWS.WebRoot*&gt;/bin/                       |
| Modern POS のローカルのハード ステーション (情報の保護とコントロール \[IPC\]) | &lt;*MPOS.AppRoot*&gt;/ClientBroker/                                      | 該当なし                           | &lt;*MPOS.AppRoot*&gt;/ClientBroker/             |
| E コマース                                                                 | 該当なし                                                            | &lt;*ECOM.WebRoot*&gt;/Connectors/       | 該当なし                                   |

上記のテーブルへのキーを次に示します。

- &lt;*Aos.PackageDirectory*&gt; は AOS のパッケージ ディレクトリです。 パスは AOS の web.config ファイルから見つけることができます (key = **Aos.PackageDirectory**)。
- &lt;*Aos.WebRoot*&gt; は AOS の Web アプリケーション ルートです。
- &lt;*RS.WebRoot*&gt; は Commerce Scale Unit の Web アプリケーション ルートです。
- &lt;*HWS.WebRoot*&gt; はリモート ハードウェア ステーションの Web アプリケーション ルートです。
- &lt;*MPOS.AppRoot*&gt; は Modern POS (例えば、\\C:Program Files (x86)\\Microsoft Dynamics AX70\\Retail Modern POS) のアプリ インストール フォルダーです。
- &lt;*ECOM.WebRoot*&gt; は電子商取引 Web サイト の Web アプリケーション ルートです。

支払 Web ファイル フォルダーには通常、サブフォルダーが含まれます。 サブフォルダー全体をターゲットの場所にコピーしてください。

## <a name="use-a-payment-connector-with-an-e-commerce-site"></a>電子商取引サイトで支払コネクタを使用

E コマース サイトは、LCS の管理された環境では配置されていません。 パートナーと連携して、電子商取引サイトをホストする方法を決定する必要があります。 支払コネクタに支払 Web ファイルが必要とされる場合は、電子商取引にこれらの Web ファイルを配置する必要があります。 支払コネクタが、支払 Web ファイルを必要としない場合、追加の手順は必要ありません。 支払 Web ファイルを電子商取引サイトに配置する方法については、このトピックの前半にある[支払コネクタ アセンブリとファイルを正しい場所に配置する](deploy-payment-connector.md#put-the-payment-connector-assemblies-and-files-in-the-correct-locations)を参照してください。

## <a name="additional-resources"></a>その他のリソース

[支払コネクタと支払デバイスの実装ガイド](https://download.microsoft.com/download/e/2/7/e2735c65-1e66-4b8d-8a3c-e6ef3a319137/The%20Guide%20to%20Implementing%20Payment%20Connector%20and%20Payment%20Device_update.pdf)

[配置可能パッケージの作成](retail-sdk/retail-sdk-packaging.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]