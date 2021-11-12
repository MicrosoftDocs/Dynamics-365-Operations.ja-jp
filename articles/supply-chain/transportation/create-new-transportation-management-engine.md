---
title: 新しい輸送管理エンジンの作成
description: このトピックでは、Dynamics 365 Supply Chain Management で新しい輸送管理エンジンを作成する方法について説明します。
author: Henrikan
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: TMSGenericEngine, TMSRateEngine, TMSMileageEngine, TMSEngineParameters
audience: Application User, Developer, IT Pro
ms.reviewer: kamaybac
ms.custom: 51661
ms.assetid: 0473acef-755e-4b42-acf5-5e5aa902dc0e
ms.search.region: Global
ms.author: henrikan
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 88661b6a974e2bd60f78e38d49a08d3290008b8b
ms.sourcegitcommit: 614d79cba238e466d445767a7d0a012e785a9861
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/19/2021
ms.locfileid: "7651547"
---
# <a name="create-a-new-transportation-management-engine"></a>新しい輸送管理エンジンの作成

[!include [banner](../includes/banner.md)]

このトピックでは、Dynamics 365 Supply Chain Management で新しい輸送管理エンジンを作成する方法について説明します。 

輸送管理 (TMS) エンジンは、輸送管理で配送率を生成およびプロセスするために使用するロジックを定義します。 Supply Chain Management は、レート、輸送時間、および輸送中に越えるゾーンの数などのさまざまなパラメーターを計算する複数の異なるエンジン タイプを提供します。 この記事では、Microsoft Visual Studio 開発環境と Supply Chain Management 開発ツールを使用して新しい TMS エンジンを作成して展開する方法と、次に Operations でエンジンを設定する方法について説明します。 エンジンに関する詳細については、[輸送管理エンジン](transportation-management-engines.md) を参照してください。

## <a name="create-a-new-tms-engine"></a>新しい TMS エンジンを作成する

このセクションでは、TMS エンジン実装を持つクラス ライブラリを作成する方法と、Supply Chain Management モデルからクラス ライブラリを参照する方法について説明します。

1. 新しいエンジンを配置するには、エンジンを含めるモデルが必要です。 **Dynamics 365**&gt; **モデル管理** メニューで、**モデルの作成** をクリックして、新しいモデルを作成します。 **モデルの作成** ウィザードの最初のページで、モデル名を **TMSEngines** にします。 

   [![モデルの作成。](./media/012.png)](./media/012.png)

2. 次のページで、**新しいパッケージの作成** を選択します。 

   [![新規パッケージの作成。](./media/021.png)](./media/021.png)

3. 次のページで、参照する **ApplicationSuite** モデルを選択します。 (**ApplicationPlatform** モデルが事前に選択されています)。 

   [![参照するモデルの選択。](./media/032.png)](./media/032.png)

4. 次のページで、**完了** をクリックして新しいモデルの作成を確認します。 

   [![モデル作成の完了。](./media/042.png)](./media/042.png)

5. 新しいソリューションで、新しい Supply Chain Management プロジェクトを作成し、**TMSThirdParty** と名前を付けます。 プロジェクト プロパティで、プロジェクトのモデルを **TMSEngines** に設定します。
6. ソリューションに新しい C\# クラス ライブラリを追加し、**ThirdPartyTMSEngines** という名前をつけます。
7. ThirdPartyTMSEngines プロジェクトで、Supply Chain Management 固有のアセンブリへの参照を追加します。
   -   X++ タイプの参照を有効にするアプリケーション アセンブリ。 これらのアセンブリは、次の場所にあります。 \[パッケージ ルート\] は、C:\\Packages など、展開されたアセンブリが配置されている場所のパスです。

        ```xpp
        [Packages root]\ApplicationPlatform\bin\Dynamics.AX.ApplicationPlatform.dll
        [Packages root]\ApplicationFoundation\bin\Dynamics.AX.ApplicationFoundation.dll
        [Packages root]\ApplicationSuite\bin\Dynamics.AX.ApplicationSuite.dll
        ```
        
   -   データ、LINQ、および補助機能へのアクセスを有効にするフレームワーク アセンブリ。 これらすべてのアセンブリは \[パッケージ ルート\]\\ 在庫置場で見つけることができます。

        ```xpp 
        Microsoft.Dynamics.ApplicationPlatform.Environment.dll
        Microsoft.Dynamics.AX.Data.Core.dll
        Microsoft.Dynamics.AX.Framework.Linq.Data.AdoNet.dll
        Microsoft.Dynamics.AX.Framework.Linq.Data.dll
        Microsoft.Dynamics.AX.Framework.Linq.Data.Interface.dll
        Microsoft.Dynamics.AX.Framework.Linq.Data.Msil.dll
        Microsoft.Dynamics.AX.Server.Core.dll
        Microsoft.Dynamics.AX.Xpp.AxShared.dll
        Microsoft.Dynamics.AX.Xpp.Support.dll
        ```

   -   コア TMS アセンブリ (エンジンを含む) と TMS ベース アセンブリ (ヘルパー、定数、データ転送クラス定義などを含む) これらのアセンブリは、次の場所にあります。

        ```xpp
        [Packages root]\ApplicationSuite\bin\Microsoft.Dynamics.AX.Tms.dll
        [Packages root]\ApplicationSuite\bin\Microsoft.Dynamics.AX.Tms.Base.dll
        ```
8. ThirdPartyTMSEngines プロジェクトで生成された C\# クラスの名前を **SampleRatingEngine** に変更します。
9. エンジンを実装します。 この例ではレート エンジンを作成しているため、レート エンジンの基本クラスを継承しています。 基本クラスは、レート エンジン インターフェイス (**TMSFwkIRateEngine**) のほとんどを実装します。 レート法の実装が必要なだけです。 この例を単純にするために、このメソッドではハードコーディングされたレートを 100 として登録します。 **TMSFwkIAccessorialEngine** などの、任意のエンジン インターフェイスを実装するエンジンを作成することができます。 すべてのエンジン インターフェイスは X++ で定義されます。

    ```xpp
    namespace ThirdPartyTMSEngines
    {
        using Dynamics.AX.Application;
        using Microsoft.Dynamics.Ax.Tms.Base.Data;
        using Microsoft.Dynamics.Ax.Tms.Base.Utility;
        using Microsoft.Dynamics.Ax.Tms.Bll;
        using System.Xml.Linq;
        public class SampleRatingEngine : BaseRateEngine
        {
            public override RatingDto rate(TmsTransactionFacade transactionFacade, XElement shipment, TMSRateMasterCode rateMasterCode)
            {
               XElement re = shipment.RetrieveOrCreateRatingEntity(this.RatingDto);
               re.AddRate(TmsRateType.Rate, 100);
               return this.RatingDto;
            }
        }
    }
    ```

10. ソリューションをビルドします。
11. TMSThirdParty プロジェクトに新しい参照を追加します。 参照は、ThirdPartyTMSEngines プロジェクトを指す必要があります。 完了したら、ソリューションは次のようになります。 

    [![TMSThirdParty プロジェクトへの参照を含むソリューション。](./media/052.png)](./media/052.png)

12. ソリューションをビルドします。 アプリケーション エクスプ ローラーの **参照** ノードに新しいライブラリが表示されていることを確認します。 

    [![アプリケーション エクスプ ローラーの参照ノード内の新しいライブラリ。](./media/061.png)](./media/061.png)

## <a name="deploy-the-tms-engine-as-a-package"></a>TMS エンジンをパッケージとして配置する

サードパーティの TMS エンジンを配置する 1 つの方法は、配置パッケージを介することです。 実稼働環境では、この方法をお勧めします。 開発環境では、次のセクション「Supply Chain Management で TMS エンジンを設定する」で説明するように手動でアセンブリをコピーできます。 エンジンをパッケージとして展開するには、次の手順を実行します。

1. **Dynamics 365** &gt; **配置** メニューで、<strong>配置パッケージの作成</strong> をクリックします。
2. **配置パッケージの作成** ダイアログ ボックスで、TMSEngines モデルを選択し、パッケージ ファイルを格納する場所のパスを入力します。 

   [![TMSEngines モデルの選択。](./media/071.png)](./media/071.png)

3. パッケージをターゲット環境に展開することができるようになりました。 チュートリアルについては、[配置可能パッケージのインストール](../../fin-ops-core/dev-itpro/deployment/install-deployable-package.md) を参照してください。

## <a name="set-up-the-tms-engine-in-supply-chain-management"></a>Supply Chain Management での TMS エンジンの設定

このセクションでは、TMS エンジンを使用するために Supply Chain Management を設定する方法、および作成した新しいエンジンをレート ショッピングで使用する方法を示します。 このセクションの例では、USMF デモ データ会社を使用しています。

1. 「新しい TMS エンジンの作成」の説明に従って、新しいエンジンを作成します。
2. ソリューションを構築します。
3. 結果のアセンブリを Supply Chain Management サーバーのバイナリの場所、\[AOSWebRoot\]bin にコピーします。 **注記:** このステップは、開発環境にのみ関連します。 実稼働環境では、配置パッケージを介して配置する必要があります。 手順については、前のセクションの「パッケージとして TMS エンジンを配置する」を参照してください。
4. Supply Chain Management では、**レート エンジン** ページで新しい評価エンジンを作成します。 エンジンは、実装したエンジン クラス ライブラリとエンジン クラスを作成して生成されたエンジン アセンブリを指す必要があります。 

   [![レート エンジン ページで新規評価エンジンの作成。](./media/081.png)](./media/081.png)

5. サンプル レート エンジンを使用する配送業者を作成します。 当社のエンジンはいかなるデータも使用しないため、レート マスターを割り当てる必要はありません。 

   [![新規出荷の配送業者の作成。](./media/092.png)](./media/092.png)

6. **工順ワークベンチの評価** ページで、**レート ショップ** をクリックします。 次のスクリーン ショットに示すように、SampleCarrier から 100.00 のレートが表示されます。 この例では、倉庫 24 から顧客 US-004 へのルートの輸送料を検索しています。 ただし、料金がハードコーディングされているために、100.00 の料金が常に表示されます。

   [![工順ワークベンチの評価。](./media/101.png)](./media/101.png)

## <a name="tips-and-tricks"></a>ヒントや秘訣

- Supply Chain Management の開発ツールを使用している場合、ソリューションに新しいプロジェクトを追加すると便利です。 このプロジェクトをスタートアップ プロジェクトとして設定した場合、デバッグ セッションを開始すると、同じデバッグ セッションで X++ と C\# コードの両方のコードをデバッグできます。
- ThirdPartyTMSEngines プロジェクトを変更して再コンパイルするたびに、アセンブリの結果をバイナリの場所に手動でコピーするか、展開パッケージを通じて展開する必要があります。 それ以外の場合、古いアセンブリを使用して実行される場合があります。
- Supply Chain Management で TMS 固有の操作を実行した後、Internet Information Services (IIS) ワーカー プロセスによって ThirdPartyTMSEngines アセンブリが、ロックされアセンブリを更新することができなくなることがあります。 この場合、w3svc プロセスを再起動します。

### <a name="whitepaper"></a>ホワイト ペーパー

詳細については、次のホワイト ペーパー (AX2012 をサポートするように記述されているが、Dynamics 365 Supply Chain Management にも適用される) をダウンロードしてください

- [輸送管理エンジンの実装と展開](https://download.microsoft.com/download/b/5/f/b5ff8fef-3918-4c1d-92d5-b67eb0971684/ImplementingAndDeployingTransportationManagementEnginesInAX.pdf)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]