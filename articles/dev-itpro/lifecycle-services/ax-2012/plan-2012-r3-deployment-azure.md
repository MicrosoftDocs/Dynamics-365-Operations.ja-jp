---
title: "Azure での Dynamics AX 2012 R3 配置の計画"
description: "Microsoft Azure に Microsoft Dynamics AX 2012 R3 を展開する前に、いくつかの点を考慮し決定する必要があります。 この記事では、計画プロセスについて説明します。"
author: kfend
manager: AnnBe
ms.date: 11/13/2017
ms.topic: article
ms.prod: dynamics-ax-2012
ms.service: 
ms.technology: 
audience: Developer, IT Pro
ms.reviewer: kfend
ms.search.scope: AX 2012
ms.custom: 18591
ms.assetid: 84e597d7-6ad3-4322-8ac3-6b6151dd24f6
ms.search.region: Global
ms.author: kfend
ms.search.validFrom: 
ms.dyn365.ops.version: 2012
ms.translationtype: HT
ms.sourcegitcommit: 879eb9f2a63a8514791f74965005ed3e22bc0de7
ms.openlocfilehash: 905084f3fdd0a18bdd4de2729fd4c6589e4bc9ea
ms.contentlocale: ja-jp
ms.lasthandoff: 04/20/2018

---

# <a name="plan-your-dynamics-ax-2012-r3-deployment-on-azure"></a>Azure での Dynamics AX 2012 R3 配置の計画

[!INCLUDE [banner](../../includes/banner.md)]

Microsoft Azure に Microsoft Dynamics AX 2012 R3 を展開する前に、いくつかの点を考慮し決定する必要があります。 この記事では、計画プロセスについて説明します。 

Azure 上の AX 2012 R3 の配備は、Microsoft が次のシナリオでサポートしています。 
- 配置は、Microsoft Dynamics Lifecycle Services (LCS) を通じて実行されています。 
- 以下のガイダンスに厳密に従って実施された顧客またはパートナー主導配置。 
   - SQL は、(SQL クラスタリング/Always On を使用して) 可用性トポロジに配置されます。
   - Azure に配置するために、[Azure 仮想マシンでの SQL Server のパフォーマンス ベスト プラクティス](/azure/virtual-machines/windows/sql/virtual-machines-windows-sql-performance)を使用して、SQL のベスト プラクティスに従っています。 
   - [SQL サーバーおよび記憶域の設定のコンフィギュレーション (TechNet)](https://technet.microsoft.com/en-us/library/dd309734.aspx) によって指定された AX 2012 の SQL Server コンフィギュレーションのベスト プラクティスに従っています。 
   - [システム診断](system-diagnostics-lcs.md)で指定されているように、システム診断ツールがインストールされ、ベスト プラクティスに従います。 

> [!NOTE]
> Azure 環境でサポートされていない AX 2012 R3 に問題があり、LCS 経由で Azure に展開された、またはローカルに展開された AX 2012 R3 環境で同じ問題を再現することができる場合、Microsoft がサポートを提供できます。
> 
> AX 2012 R3 は、オンプレミスでも配置できます。 詳細については、トピックの [Microsoft Dynamics AX 2012 のインストール](https://technet.microsoft.com/en-us/library/dd362138.aspx) を参照してください。

## <a name="verify-that-you-can-log-on-to-lifecycle-services"></a>Lifecycle Services にログオンできることを確認します。
Lifecycle Services (LCS) は、顧客およびパートナーが Microsoft Dynamics AX のプロジェクトの管理に使用できるクラウドベースの共同ワークスペースです。 Azure 上に AX 2012 R3 を配置するには、Lifecycle Services Web サイトで利用できるクラウド ホスト環境ツールを使用します。 Lifecycle Services は顧客やパートナーがサポート計画の一部として使用できます。 CustomerSource または PartnerSource の資格情報でアクセスすることができます。 [Lifecycle Services にログオンできることを確認する](https://lcs.dynamics.com/)

## <a name="purchase-an-azure-subscription"></a>Azure サブスクリプションの購買
Azure を使用するには、サブスクリプションを購入する必要があります。 サブスクリプション プランおよび価格決定の詳細については、[Azure 価格決定](https://azure.microsoft.com/en-us/pricing/) ページを参照してください。 その後、そのページの指示に従ってサブスクリプションを購入します。 サブスクリプションは、Azure に配備する AX 2012 R3 環境をサポートするのに十分な大きさでなければなりません。 次のテーブルは、Azure に配置できる AX 2012 R3 環境のタイプと、各環境を既定のコンフィギュレーションで配置するために必要なコアの数を示しています。 

> [!NOTE]
> 環境を配置するときに、配置される仮想マシンの数とサイズを変更できることに留意してください。 ただし、次のテーブルでは、その*既定*コンフィギュレーションで各環境を配置するために必要なコアの数を一覧にします。

**環境タイプ:** - デモ


| 環境名       | 既定の構成で環境を配置するコアの数 |
|------------------------|------------------------------------------------------------------------|
| AX 2012 R3 デモ        | 8 コア                                                                |
| AX 2012 R3 CU8 デモ    | 8 コア                                                                |
| Retail Essentials デモ | 8 コア                                                                |


**環境タイプ:** - 開発/テスト


| 環境名                   | 既定の構成で環境を配置するコアの数 |
|------------------------------------|------------------------------------------------------------------------|
| 開発                        | 9 コア                                                                |
| 共有 SQL Server による開発 | 14 コア                                                               |
| テスト                               | 13 コア                                                               |
| Retail Essentials 開発/テスト         | 4 コア                                                                |
| Retail E-commerce 開発/テスト         | 4 コア                                                                |
| Retail Mobility 開発/テスト           | 4 コア                                                                |


**環境タイプ:** - 高可用性


| 環境名              | 既定の構成で環境を配置するコアの数 |
|-------------------------------|------------------------------------------------------------------------|
| 高可用性環境 | 45 コア                                                               |


Azure のサブスクリプションを既に持っている場合、次に注意します。

-   **定期売買のサイズを表示する:** Azure 管理ポータルで、定期売買のサイズを表示することができます。 これを行うには、[[Azure管理ポータル](https://manage.windowsazure.com/)] にログオンし、**設定**&gt;**使用** をクリックします。
-   **定期購読のサイズを増やす:** 定期売買のサイズを増やすには、Azure サポート チームにてサポート チケットを作成する必要があります。 これを行うには、[[Azure サポート オプション](http://azure.microsoft.com/en-us/support/options/)] ページに移動し、**サポートを受ける** をクリックしてサポート チケットを作成します。 サポート チケットを作成するとき、チケットが課金サポートに対応していることを確認します。

> [!NOTE]
> クラウド ソリューション プロバイダー (CSP) プログラムは、Azure Resource Manager (ARM) 要件のため Lifecycle Services によって現在サポートされていません。

## <a name="purchase-and-azure-support-plan"></a>発注書および Azure サポート計画
Azure サポート計画では Azure の技術および課金サポートを提供します。 Azure サポート プランは、Azure 展開のサポーの適切なレベルを選択できる柔軟なサポート オプションを提供しています。 サポート オプションには、Azure サブスクリプションに含まれているサポート サービスから、無料のサポート サービスまでさまざまです。 利用可能なサポート プランについて学び、プランを購入するには、[[Azure サポート計画](http://www.windowsazure.com/en-us/support/plans/)] ページをご覧ください。

## <a name="become-familiar-with-the-azure-management-portal"></a>Azure 管理ポータルを使いこなせるようになります
Azure 管理ポータルは、開発者および IT プロフェッショナルに、その Azure コンポーネントをプロビジョニング、構成、監視、および管理する機能を提供します。 今後使用するために、管理ポータルについてよく理解しておくことが重要です。

-   管理証明書をアップロードします。 (管理証明書を使用すると、Lifecycle Services はユーザーに代わって Azure に AX 2012 R3 環境を配置できます。)
-   仮想マシンに接続します。
-   AX 2012 R3 環境の正常性および状態を監視します。

Azure サブスクリプションを購入した後、[ここ。](https://manage.windowsazure.com/?whr=live.com) をクリックして管理ポータルにアクセスできます。 次の図は、管理ポータルを示しています。 [![PlanYouAXR3DeploymentonAzure1](./media/planyouaxr3deploymentonazure1.jpg)](./media/planyouaxr3deploymentonazure1.jpg)  

## <a name="become-familiar-with-the-azure-vm-agent"></a>Azure VM エージェントを使いこなせるようになります
Azure VM エージェントは、Lifecycle Services を通じて展開されたすべての VM で自動的に配置されます。 Azure VM エージェントは、Azure 仮想マシン拡張 (VM 拡張) インストール、コンフィギュレーション、管理、実行するために使用されます。 VM 拡張機能は、VM を監視および管理するのに役立ちます。

## <a name="consider-cloud-services-resource-requirements"></a>クラウド サービスのリソース要件を検討する
トポロジが配置されると、配置システムは選択された仮想マシン (VM) の SKU を検査します。 Azure がこれらの VM を VM が使用可能である適切なクラスターに配置していることを確認するために、VM SKU の各レベルに独自の Azure クラウド サービスが必要です。 VM SKU の内訳は次のとおりです。

|         |                                 |
|---------|---------------------------------|
| **最小在庫管理単位** | **サイズ**                        |
| A       | 標準 A の \[A0-A4\]          |
| 午前      | 標準 A の \[A5-A7\]          |
| AL      | 標準 A の (大) \[A8-A11\] |
| D       | 標準 D の\[すべての D シリーズ\]   |
| DS      | 標準 DS の\[すべての DS シリーズ\] |
| G       | 標準 G の\[すべての G シリーズ\]   |

Version-Topology-EnvironmentName-SKU-GUID という名前付けスキームを含むクラウド サービスが作成されます。必要に応じて、配置のためのクラウド サービス リソース要件を検討し、Azure サポートから Azure サブスクリプションの追加クラウド サービス能力を要求してください。

## <a name="plan-for-storage-accounts"></a>ストレージ アカウントの計画
Lifecycle Services で作成された各プロジェクトについては、1 つまたは複数の個別のストレージ アカウントが Azure 定期売買で作成されます。 ストレージ アカウントは、プロジェクトを Azure サブスクリプションに接続すると作成されます。 このストレージ アカウントは、ローカル冗長ストレージ (LRS) アカウントであり、展開に必要なスクリプトと VHD を格納するために使用されます。 最初の Premium ストレージ有効トポロジがプロジェクトから配置されると、各プロジェクトが作成され Premium ストレージ アカウントが追加されます。 ストレージ アカウントは、配置が同じ Azure サブスクリプションに行われる場合でも、Lifecycle Services プロジェクト間で共有されません。 Premium ストレージ アカウントが作成されると、それもまた LRS として作成されます。 ストレージの詳細については、[ここ](http://azure.microsoft.com/en-us/pricing/details/storage) をクリックしてください。 同じ Lifecycle Services (LCS) プロジェクトと Azure コネクタに展開されるトポロジと環境の数を検討します。 Premium ストレージ アカウントとは別に、既定では、LCS プロジェクトおよび Azure コネクタごとにストレージ アカウントが 1 つ存在します。 Azure Storage には[限度](https://azure.microsoft.com/en-us/documentation/articles/azure-subscription-service-limits/#storage-limits)があるので注意してください。具体的には、標準ストレージ アカウントあたり 20,000 IOPS (秒単位の入力/出力オペレーション) です。 VHD あたり 500 IOPS と組み合わせると、調整が発生する前に約 40 個の***利用効率が高い*** VHDが残されます。 これを軽減するには、複数の Azure コネクタや複数の LCS プロジェクトを活用することをお勧めします。 たとえば、1 つの LCS プロジェクトで製造環境を、別で開発/テスト環境を検討します。 

> [!NOTE]
> インストール VHD など、LCS が配置するすべての VHD が高度に使用されるわけではありません。

## <a name="plan-your-sql-server-configuration"></a>SQL Server 構成の計画
Azure Premium Storage は、Azure 仮想マシン (VM) 上で実行される I/O 集約型ワークロードに対して高パフォーマンス、待機時間が短いディスク サポートを提供します。 Premium Storage では、アプリケーションは VM ごとに 32 TB までのストレージを持つことができ、VM ごとに 50,000 IOPS を達成し、読み取り操作での待機時間は非常に短くなります。 Premium Storage は、生産能力で使用される AX 2012 R3 配置に必要です。 Azure DS シリーズ VM が選択されている場合、高可用性配置では Premium Storage が既定で有効になります。 Premium Storage は、現時点では DS シリーズ VM 上でのみ提供されています。 他のすべての記憶域ニーズに非 Premium ストレージが使用されているとき、SQL Server AlwaysOn データベース サーバーだけで Premium Storage が有効になります。 SQL Server AlwaysOn 可用性セットが作成されると、Lifecycle Services は、選択された DS シリーズ VM でサポートされているすべてのディスク スロットに対してディスクをアタッチします。 VM ディスク能力の詳細については、[ここ](https://msdn.microsoft.com/en-us/library/azure/dn197896.aspx) をクリックします。 異なる VM サイズには、スループットと IOPS の最大値が変化します。 結果として、 SQL Server の構成を計画しているときは、ビジネスに最も効率的でコスト効果の良いソリューションを展開するために、これらの制限に精通してください。 [Premium Storage: Azure 仮想マシン ワークロード向け高性能ストレージ](https://azure.microsoft.com/en-us/documentation/articles/storage-premium-storage-preview-portal/)に関するページ (特に、**Premium Storage の使用時の調整**に関するセッション) にあるガイドラインに従ってください。 SQL Server AlwaysOn 可用性セットは、Lifecycle Services を通じて自動的に作成されます。 生産システムで使用するための高可用性トポロジを配置する前に、データおよびパフォーマンスのニーズを考慮することが重要です。 Azure Premium Storage については、[こちら](http://azure.microsoft.com/en-us/documentation/articles/storage-premium-storage-preview-portal/)をご覧ください。 Premium Storage で配置を計画すると、高可用性トポロジには、原価とパフォーマンスの目標を達成するためのコンフィギュレーション オプションが提供されます。 高可用性のトポロジの詳細設定では、次の SQL Server 構成オプションが表示されます。

-   **SQL Server イメージ コンフィギュレーションのカスタマイズ** - このオプションを使用すると、カスタム SQL Server Enterprise イメージまたは Azure Gallery SQL Server Enterprise イメージを使用できます。
    -   カスタム SQL Server イメージ (既定) - このイメージには、SQL Server Enterprise 2014の試用版が含まれています。 評価版ライセンスは 3〜6 か月間有効です。 既存の EA/etc. ライセンスを使用する場合は、このオプションを使用します。
    -   ギャラリー SQL Server イメージ – このイメージには SQL Server Enterprise 2014 が含まれており、消費に基づく Azure 価格決定を使用します。 詳細については、[Azure 仮想マシンの価格決定](https://azure.microsoft.com/en-us/pricing/details/virtual-machines/#sql-server)ページと [Azure 仮想マシンの SQL Server](https://msdn.microsoft.com/library/azure/jj823132.aspx) で確認できます。
-   **SQL Server のストレージ領域コンフィギュレーションのカスタマイズ** - SQL Server VM に関連付けられるディスクの数とサイズを指定できます。

SQL Server 内でストレージ領域の作成に使用する必要があるディスクの数を指定する場合は、次の点に留意してください。

-   データベース サーバーのために選択されている VM サイズで、その VM SKU でサポートされるディスクの数が決まります。 各 VM でサポートされているディスクの数に関する情報は、[ここ](https://msdn.microsoft.com/en-us/library/azure/dn197896.aspx)で確認できます。
-   VM で使用可能なディスク スロットの 1 つは、Lifecycle Services 配置サービスで使用されます。 これは、VM の最大ディスク数 (マイナス1) が、使用可能なスロットを満たすことを意味します。
-   この設定を空白のままにすると、配置サービスによって VM でサポートされている最大までディスクを関連付けることができます。 最大のディスクが使用される運用配置の場合にお勧めします。

VM に関連付けられている各ディスクのサイズ (GB 単位) を指定する場合、次の点に留意してください。

-   100 GB – 1024 GB 値を許可します。
-   既定値は 128 GB です。
-   使用されるディスクのサイズは、使用される Premium Storage 階層を決定します。
-   Premium Storage 層は、原価、ディスクあたりの IPOPS、および展開されるシステムのスループットを示しています。 詳細については、[ここ](http://azure.microsoft.com/en-us/pricing/details/storage/) をクリックしてください。
-   すべてのディスクは 64k クラスター サイズにフォーマットします。 これにより、パフォーマンスが最大 20％ 向上します。 詳細については、[ここ](http://tk.azurewebsites.net/2012/08/) をクリックしてください。

TempDB とログは、パフォーマンスの向上のために記憶域上に配置されます。 そのストレージ領域にコンフィギュレーションされているディスクの数に対して、1 つの仮想ディスクが作成されます。 次に、仮想ディスクは次のようにパーティション化されます。

-   SQL データ = プールの合計サイズの 1/2
-   SQL ログ = 合計サイズの 1/4
-   SQL Temp db = 合計サイズの 1/8
-   SQL バックアップ = 合計サイズの残り 1/8

他の考慮事項を念頭に置く必要があります。

-   配置を計画するときは、対象とする Azure 領域で Premium Storage を使用できることを確認します。 詳細については、[ここ](http://azure.microsoft.com/en-us/services/preview/) をクリックしてください。
-   会社のネットワークと Azure の間で VPN/Express ルート接続 (または計画) がある場合、Premium ストレージ アカウントをサポートしている Azure 地域でこれが行われていることが確認します。
-   使用に関する制限について理解するためには [Azure Premium Storage ドキュメント](http://azure.microsoft.com/en-us/documentation/services/storage/) を参照してください。
-   可用性トポロジーで非 Premium ストレージ VM がデプロイされている場合は、上記のすべての SQL Server のコンフィギュレーションを適用できますが、Premium ストレージのメリットは適用されません。
-   配置ために Lifecycle Services プロジェクトを設定するとき、Premium Storage をサポートする地域を選択する必要があります。

展開サービスにより実装される SQL Server ベスト プラクティスには、SQL Server チームにより推奨されるベスト プラクティスが含まれます。 詳細については、[ここ](http://blogs.technet.com/b/dataplatforminsider/archive/2014/09/12/new-vm-images-optimized-for-transactional-and-dw-workloads-in-azure-vm-gallery.aspx) をクリックしてください。 さらに、次の項目が実行されます。

-   複数の一時ファイル (CPU コアごとに 1 つ)。
-   SQL Server の最大メモリを使用可能なコンピューター RAM の 90% に設定します。
-   並列処理の最大限度を設定します。
-   トレース フラグの有効  -T1204、 -T1222。

## <a name="estimate-costs-and-understand-the-azure-billing-process"></a>減価を見積もり、Azure 請求プロセスに同意
Azure での AX 2012 R3 の展開コストを見積もるには、[[Azure 価格計算ツール](http://azure.microsoft.com/en-us/pricing/calculator/)] を使用します。 Azure に AX 2012 R3 を配置する前に、Azure 請求プロセスについて理解することも重要です。 サンプル請求書、および現在の請求期間に対する毎日の使用データをダウンロードする方法に関する情報にリンクする Azure 請求プロセスの概要については、[請求書を理解する](http://azure.microsoft.com/en-us/support/understand-your-bill/) を参照してください。 **注記:** 使用されていないときに Azure 上に配置されている AX 2012 R3 環境をシャット ダウンすることができることに留意してください。 たとえば、コスト削減のため週末に環境をシャット ダウンする場合があります。 環境をシャット ダウンすると、その環境はまだ存在します。ただし、その環境内の仮想マシンはシャット ダウンされます。 仮想マシンが実行されていないときは、それに対して課金されません。 詳細については、「環境をシャット ダウンする方法とは」を参照してください。 [Azure 上の Microsoft Dynamics AX 2012 R3 配置の管理](manage-2012-r3-deployment-azure.md) の記事にあります。

## <a name="consider-legal-and-regulatory-requirements"></a>法的および規制要件を考慮する
Microsoft は、複数の地域や税務署にわたる一般的な運用方法と機能で Azure サービスを実行します。 ただし、Microsoft サービスがユーザーの規制の必要を満たしているかどうかを判断するのは、最終的にはユーザー次第となります。 最新の情報を提供するために、[Azure セキュリティ センター](http://azure.microsoft.com/en-us/support/trust-center/) はセキュリティ、プライバシー、コンプライアンスに関する以下の情報を提供します。

-   **セキュリティ**、[Azure セキュリティ ページ](http://www.windowsazure.com/en-us/support/trust-center/security/) は地理的に分散されているデータ センター内に安全な環境を提供するために Microsoft が取っている条項の概要を示します。 セキュリティ関連リソースの広範なリストの中で、[情報の要求についての標準応答: セキュリティおよびプライバシー](https://www.microsoft.com/en-us/download/details.aspx?id=26647) ホワイト ペーパーがどのように Azure の提案されたプリンシパルを満たし、国際標準化機構 (ISO) 27001:2005 および ISO 27002 にマップされているかを概説します。
-   **プライバシー** [Azure プライバシー ページ](http://www.windowsazure.com/en-us/support/trust-center/privacy/) Azure 環境のプライバシーに関する取り組みを説明する複数のリソースへのリンクが含まれています。 [Azure のプライバシーに関する声明](http://www.windowsazure.com/en-us/support/legal/privacy-statement/)へのリンクが含まれています。
-   **コンプライアンス** [Azure コンプライアンス ページ](http://www.windowsazure.com/en-us/support/trust-center/compliance/)は、独自の業界に適用される特定の法律および規制を順守し、シナリオを使用するためのリソースを提供します。

## <a name="consider-licensing-requirements"></a>ライセンス供与の要件の検討
AX 2012 R3 仮想マシン環境のさまざまなコンポーネントのライセンス供与は、重要な考慮事項です。 Azure での展開は、 Azure に固有な特別なライセンス条項であるか、およびそれらの条項がソリューションの全体的な適合性を備えているかを評価します。 ライセンス供与の要件は、Azure に配置する AX 2012 R3 仮想マシン環境の種類によって異なります。 次のテーブルに詳細を示します。

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><strong>環境のタイプ</strong></td>
<td><strong>ライセンス要件</strong></td>
</tr>
<tr class="even">
<td>デモ</td>
<td>仮想マシン環境に含まれるソフトウェアは、ソフトウェア ライセンス条項の項目に従って、時間制限付きで使用許諾されます。
<ul>
<li><a href="http://go.microsoft.com/fwlink/?LinkId=397371">AX 2013 R3 デモ環境のソフトウェア ライセンス条項</a></li>
<li><a href="http://go.microsoft.com/fwlink/?LinkId=397371">AX 2013 R3 CU8 デモ環境のソフトウェア ライセンス条項</a></li>
<li><a href="http://go.microsoft.com/fwlink/?LinkId=397371">5. Retail Essentials デモ環境のソフトウェア ライセンス条項</a></li>
</ul></td>
</tr>
<tr class="odd">
<td>開発/テストおよび高可用性</td>
<td>仮想マシン環境を含めすべてのソフトウェアには適切なライセンスが必要です。 パートナーとマイクロソフトの担当者共に、ライセンスのニーズを十分に調査してください。 仮想マシン環境に含まれる個々のソフトウェアの条件を調査する必要があります。 仮想マシン環境に含まれるソフトウェアの完全な一覧については、ソフトウェア ライセンス条項を参照してください。
<ul>
<li><a href="http://go.microsoft.com/fwlink/?LinkId=397363">開発環境のソフトウェア ライセンス条項</a></li>
<li><a href="http://go.microsoft.com/fwlink/?LinkId=397363">共有の SQL Server 環境による開発用のソフトウェア ライセンス条件</a></li>
<li><a href="http://go.microsoft.com/fwlink/?LinkId=397363">テスト環境のソフトウェア ライセンス条項</a></li>
<li><a href="http://go.microsoft.com/fwlink/?LinkID=507496&amp;amp;clcid=0x409">5. Retail Essentials 開発/テスト環境のソフトウェア ライセンス条項</a></li>
<li><a href="http://go.microsoft.com/fwlink/?LinkID=507494">5. Retail E-commerce 開発/テスト環境のソフトウェア ライセンス条項</a></li>
<li><a href="http://go.microsoft.com/fwlink/?LinkID=507496">5. Retail Mobility 開発/テスト環境のソフトウェア ライセンス条項</a></li>
<li><a href="http://go.microsoft.com/fwlink/?LinkId=397363">高可用性環境のソフトウェア ライセンス条項</a>ライセンス条項と要件を確認する際には、Azure に配置するために特に適用される条項、および使用目的に適用される条項に特に注意する必要があります。 たとえば、Microsoft Office は Azure に固有の条件を持ちますが、これらの条件は、開発またはテスト目的で Office を配置するか、または生産目的で Office を配置するかどうかによって異なります。</li>
</ul>
開始するうえで役立ついくつかのリソースを以下のリンクに示します。 以下にリンクされているリソースのほとんどに、複数の製品およびシナリオの詳細な情報へのリンクが含まれています。ただし、追加の情報を確認しなければならない場合があります。 この情報は、ライセンスを取得した製品の承認済みの使用に関するガイドに役立つ情報です。 同意ではありません。 ボリューム ライセンス契約にもとづいてライセンスされている製品の使用は、その契約の条件によって支配されます。 ここにリンクされている情報と契約に矛盾がある場合、契約の使用条件が有効となります。
<ul>
<li><strong>仮想マシン ライセンスによく寄せられる質問</strong> Azure 仮想マシンのライセンスに関するよくある質問は、<a href="http://www.windowsazure.com/en-us/pricing/licensing-faq/">このページ</a>で回答されています。</li>
<li><strong>Microsoft 製品の使用権限と製品リスト</strong>ビジネス上の意思決定を効果的にし、IT 購入価値を最大化するために、<a href="http://go.microsoft.com/fwlink/?LinkId=397363">このページ</a>で、Microsoft ボリューム ライセンス製品のライセンスモデル、プログラム、シナリオ、および使用条件について詳細を確認します。</li>
</ul>
<ul>
<li><strong>Azure プログラムのソフトウェア保証によるライセンス モビリティ</strong>ソフトウェア保証によるライセンス モビリティにより、Microsoft ボリューム ライセンスの顧客は、Azure でアクティブなソフトウェア保証を使用して、適格なサーバー アプリケーションを配置する柔軟性を得ることができます。 このソフトウェア保証給付金では、新しいライセンスを購入する必要がなく、関連するモビリティ費用がかかりません。 これにより、既存のライセンスを Azure クラウド プラットフォームに簡単に展開できます。 詳細については、<a href="http://www.windowsazure.com/en-us/pricing/license-mobility/">このページ</a>を参照してください。 開発、テスト、および SharePoint の高可用性トポロジ トライアル版用に、Visual Studio、SQL Server および Office が提供されています。 評価の範囲は 30〜180 日間です。 それに応じてライセンスを適用してください。</li>
<li><strong>Microsoft Dynamics AX ボリューム ライセンス バイヤー ガイド </strong>Microsoft Dynamics AX を使用したキー ライセンス オプションの概要については、<a href="http://go.microsoft.com/fwlink/?LinkId=397363">このページ</a>を参照してください。</li>
<li><strong>Office 365 ProPlus の共有コンピュータの有効化</strong>共有コンピューターの有効化により、複数のユーザーがアクセスする組織内のコンピュータに Office 365 ProPlus を配置できます。 詳細については、<a href="https://technet.microsoft.com/en-us/library/dn782860(v=office.15).aspx">このページ</a>を参照してください。</li>
</ul></td>
</tr>
</tbody>
</table>

## <a name="select-the-ax-2012-r3-environment-that-you-want-to-deploy"></a>配置する AX 2012 R3 環境を選択
Azure 上に AX 2012 R3 環境を配置するには、Lifecycle Services のクラウド ホスト環境ツールを使用します。 クラウド ホスト環境ツールを使用して配置するとき、デモまたは開発/テスト環境などの、Azure 上に配置する環境のタイプを選択する必要があります。 この選択に基づいて、クラウド ホスト環境ツールは Azure での仮想マシンの適切な数を提供します。 これらの仮想マシンには、AX 2012 R3 コンポーネント (およびそれらの必要物すべて) がインストール済みです。 次のセクションでは、Azure に配置できる AX 2012 R3 環境について説明します。

-   AX 2012 R3 および AX 2012 R3 CU8 デモ環境
-   Retail Essentials デモ環境
-   開発環境
-   テスト環境
-   Retail Essentials 開発/テスト環境
-   Retail E-commerce 開発/テスト環境
-   Retail mobility 開発/テスト環境
-   高可用性環境

> [!NOTE]
> このような環境では、SQL Server は SQL\_Latin1\_General\_CP1\_CI\_AS の照合順序を使用するよう構成されます。

## <a name="ax-2012-r3-and-ax-2012-r3-cu8-demo-environments"></a>AX 2012 R3 および AX 2012 R3 CU8 デモ環境
2 つの AX 2012 R3 デモ環境があります。1 方の環境には累積更新プログラム 8 があり、もう 1 つ方にはありません。 次のテーブルは、それぞれの環境に関する詳細を示します。 

> [!NOTE]
> 各環境に含まれる仮想マシンは、単一インスタンスの仮想マシンです。 シングル インスタンス仮想マシンは、Azure [サービス レベル アグリーメント](http://azure.microsoft.com/en-us/support/legal/sla/)の対象となりません。

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<tbody>
<tr class="odd">
<td><strong>既定で配置される仮想マシンの数</strong></td>
<td><strong>説明</strong></td>
<td><strong>サイズと名前</strong></td>
<td><strong>ソフトウェア インストール済み</strong></td>
</tr>
<tr class="even">
<td>1</td>
<td>デモ マシン</td>
<td><strong>サイズ:</strong>D3: 標準計算層 (4 コア、14 GB メモリ) <strong>既定名:</strong>DEMO-&lt;GUID&gt;</td>
<td><ul>
<li>Windows Server 2012 R2、以下を含む:
<ul>
<li>Active Directory</li>
<li>ドメイン名サービス (DNS)</li>
<li>インターネット インフォメーション サービス (IIS)</li>
<li>リモート デスクトップ サービス</li>
</ul></li>
<li>Microsoft Visual Studio 2013</li>
<li>Microsoft SQL Server 2014 のコンポーネント:
<ul>
<li>データベース エンジン サービス</li>
<li>レポート サービス</li>
<li>分析サービス</li>
<li>Management Studio</li>
<li>開発者ツール</li>
</ul></li>
<li>Microsoft SharePoint Server 2013</li>
<li>Microsoft Office 2013</li>
<li>AX 2012 R3 または AX 2012 R3 CU8 コンポーネント:
<ul>
<li>データベース</li>
<li>サーバー コンポーネント:
<ul>
<li>Application Object Server (AOS)</li>
<li>Web サーバー コンポーネント:
<ul>
<li>エンタープライズ ポータル (EP)</li>
<li>エンタープライズ検索</li>
<li>ヘルプ サーバー</li>
</ul></li>
</ul></li>
<li>ビジネス インテリジェンス コンポーネント:
<ul>
<li>Reporting Services 拡張機能</li>
<li>Analysis Services の構成</li>
</ul></li>
<li>Management Reporter コンポーネント:
<ul>
<li>Management Reporter サーバー コンポーネント</li>
<li>Management Reporter レポート デザイナー</li>
</ul></li>
<li>クライアント コンポーネント:
<ul>
<li>クライアント</li>
<li>Office アドイン</li>
<li>リモート デスクトップ サービス統合</li>
</ul></li>
<li>開発者ツール:
<ul>
<li>デバッガー</li>
<li>Visual Studio Tools</li>
<li>Trace Parser</li>
</ul></li>
<li>統合コンポーネント:
<ul>
<li>IIS 上の Web サービス</li>
<li>.NET Business Connector</li>
</ul></li>
<li>管理ユーティリティ</li>
<li>小売コンポーネント:
<ul>
<li>Retail POS</li>
<li>Retail Headquarters</li>
<li>Commerce Data Exchange コンポーネント:
<ul>
<li>Synch Service</li>
<li>Real-time Service</li>
<li>Async Server</li>
<li>Async Client</li>
</ul></li>
<li>Retail チャンネル コンフィギュレーション ユーティリティ</li>
<li>Retail SDK</li>
<li>小売オンライン チャネル</li>
<li>Retail サーバー</li>
<li>Retail 一括配置ツールキット</li>
<li>Retail チャンネル データベース</li>
</ul></li>
<li>RapidStart Connector</li>
<li>データのインポート/エクスポート フレームワーク コンポーネント。
<ul>
<li>データのインポート/エクスポート フレームワーク (DIXF) サービス</li>
<li>AOS コンポーネント</li>
<li>クライアント コンポーネント</li>
</ul></li>
<li>倉庫モバイル デバイス ポータル</li>
<li>Microsoft Dynamics Connector</li>
</ul></li>
</ul></td>
</tr>
</tbody>
</table>



## <a name="retail-essentials-demo-environment"></a>Retail Essentials デモ環境
この環境を配置して、Retail Essentials をデモしてください。 Retail Essentials は、Microsoft Dynamics AX の小売中心のコンフィギュレーション オプションです。 この環境には、既定で 1 台の仮想マシンが含まれます。 この仮想マシンには、Windows Server と、Retail Essentials をデモンストレーションするために必要なソフトウェアとサンプル データが既にインストールされています。 次のテーブルは、既定の Retail Essentials デモ環境の詳細を示しています。 環境を配置するとき、環境に追加の仮想マシンを追加する、または仮想マシンのサイズを変更することができます。 

> [!NOTE]
> この環境の仮想マシンは、単一インスタンスの仮想マシンです。 シングル インスタンス仮想マシンは、Azure [サービス レベル アグリーメント](http://azure.microsoft.com/en-us/support/legal/sla/)の対象となりません。

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<tbody>
<tr class="odd">
<td><strong>既定で配置される仮想マシンの数</strong></td>
<td><strong>説明</strong></td>
<td><strong>サイズと名前</strong></td>
<td><strong>ソフトウェア インストール済み</strong></td>
</tr>
<tr class="even">
<td>1</td>
<td>Retail Essentials デモ コンピューター</td>
<td><strong>サイズ:</strong>D3: 標準計算層 (4 コア、14 GB メモリ) <strong>既定名:</strong>DEMO-&lt;GUID&gt;</td>
<td><ul>
<li>Windows Server 2012 R2</li>
<li>Microsoft SQL Server 2014 のコンポーネント:
<ul>
<li>データベース エンジン サービス</li>
<li>Management Studio</li>
<li>開発者ツール</li>
</ul></li>
<li>AX 2012 R3 コンポーネント:
<ul>
<li>データベース</li>
<li>サーバー コンポーネント:
<ul>
<li>Application Object Server (AOS)</li>
</ul></li>
<li>クライアント コンポーネント:
<ul>
<li>クライアント</li>
</ul></li>
<li>統合コンポーネント:
<ul>
<li>.NET Business Connector</li>
</ul></li>
<li>小売コンポーネント:
<ul>
<li>Retail Headquarters</li>
<li>Commerce Data Exchange コンポーネント:
<ul>
<li>Real-time Service</li>
<li>Async Server</li>
<li>Async Client</li>
</ul></li>
<li>Retail チャンネル データベース</li>
</ul></li>
</ul></li>
</ul></td>
</tr>
</tbody>
</table>



## <a name="development-environments"></a>開発環境
多くの開発者の開発努力を迅速に開始する必要がある場合は、これらの開発環境を配置します。 各開発者の開発用仮想マシン (VM) を数日ではなく数時間で展開します。 開発環境には、テスト環境と同じドメインおよび仮想ネットワーク カスタマイズすべてが用意されています。 開発者シナリオには 2 つのトポロジ オプションが用意されています。

-   開発。Active Directory と共に展開されたオールインワンの VM を含みます。
-   共有 SQL Server による開発。Active Directory と共に展開されたオールインワンの VM を含みます。 各開発 VM インスタンスのデータベースは、共有 SQL Server インスタンスに配置されます。

それらの BI 開発の実行については、目的に対する 1 つのインスタンスを配置することができます。 その他のすべてのインスタンスは BI で配置されません。 提供されている開発用 VM には、すべての AX 2012 R3 コンポーネントが Visual Studio 2013 および AX 2012 R3 開発ツールとともにインストールされています。 VM は、展開時に Active Directory ドメインに結合されます。 カスタマイズ オプションとして Active Directory ドメインを指定する場合は、VM はそのドメインに参加します。 開発 VM は、AX 2012 R3 チェックリストの時点まで配置され、すべてのソフトウェアがインストールされていることがテスト環境にリストされます。 

> [!NOTE]
> この環境の仮想マシンは、単一インスタンスの仮想マシンです。 シングル インスタンス仮想マシンは、Azure [サービス レベル アグリーメント](http://azure.microsoft.com/en-us/support/legal/sla/)の対象となりません。

## <a name="test-environment"></a>テスト環境
この環境には、既定で数台の仮想マシンが含まれます。 これらの仮想マシンには、すでにインストールされている Windows Server および AX 2012 R3 のテストに必要なソフトウェアがあります。 次のテーブルは、既定のテスト環境の詳細を示しています。 環境を配置するとき、環境に追加の仮想マシンを追加する、または仮想マシンのサイズを変更することができます。 

> [!NOTE]
> この環境の仮想マシンは、単一インスタンスの仮想マシンです。 シングル インスタンス仮想マシンは、Azure [サービス レベル アグリーメント](http://azure.microsoft.com/en-us/support/legal/sla/)の対象となりません。 データのインポート/エクスポート フレームワーク (DIXF) コンポーネントは既定ではインストールされていません。 DIXF を使用する場合は、独自の SQL Server インストール メディアを使用して、SQL Server マシンに SQL Server Integration Services (SSIS) をインストールする必要があります。 SSIS をインストールした後は、Dynamics AX CD (VM 内の接続されたドライブで利用可能) を使用し、DIXF コンポーネントを AOS およびクライアント マシンにインストールできます。

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<tbody>
<tr class="odd">
<td><strong>既定で配置される仮想マシンの数</strong></td>
<td><strong>説明</strong></td>
<td><strong>サイズと名前</strong></td>
<td><strong>ソフトウェア インストール済み</strong></td>
</tr>
<tr class="even">
<td>1</td>
<td>ドメイン コントローラー</td>
<td><strong>サイズ:</strong>D1: 基本的な計算層 (1 コア、3.5 GB メモリ) <strong>既定名:</strong>AD-&lt;GUID&gt;</td>
<td><ul>
<li>Windows Server 2012 R2、以下を含む:
<ul>
<li>Active Directory</li>
<li>ドメイン名サービス (DNS)</li>
</ul></li>
</ul></td>
</tr>
<tr class="odd">
<td>1</td>
<td>AOS サーバー</td>
<td><strong>サイズ:</strong>D3: 標準計算層 (4 コア、14 GB メモリ) <strong>既定名:</strong>AOS-&lt;GUID&gt;</td>
<td><ul>
<li>Windows Server 2012 R2、以下を含む:
<ul>
<li>インターネット インフォメーション サービス (IIS)</li>
</ul></li>
<li>Microsoft Visual Studio 2013</li>
<li>Microsoft Project Server</li>
<li>Microsoft SQL Server 2014 のコンポーネント:
<ul>
<li>Management Studio</li>
<li>ネイティブ クライアント</li>
</ul></li>
<li>AX 2012 R3 または AX 2012 R3 CU8 コンポーネント:
<ul>
<li>サーバー コンポーネント:
<ul>
<li>Application Object Server (AOS)</li>
</ul></li>
<li>クライアント コンポーネント:
<ul>
<li>クライアント</li>
<li>Office アドイン</li>
<li>リモート デスクトップ サービス統合</li>
</ul></li>
<li>統合コンポーネント:
<ul>
<li>IIS 上の Web サービス</li>
<li>.NET Business Connector</li>
</ul></li>
<li>管理ユーティリティ</li>
<li>小売コンポーネント:
<ul>
<li>Retail Headquarters</li>
<li>Commerce Data Exchange コンポーネント:
<ul>
<li>Synch Service</li>
<li>Real-time Service</li>
<li>Async Server</li>
</ul></li>
</ul></li>
<li>RapidStart Connector</li>
</ul></li>
</ul></td>
</tr>
<tr class="even">
<td>1</td>
<td>データベース サーバー/BIサーバー</td>
<td><strong>サイズ:</strong>D3: 標準計算層 (4 コア、14 GB メモリ) <strong>既定名:</strong>SQL-&lt;GUID&gt;</td>
<td><ul>
<li>Windows Server 2012 R2</li>
<li>Microsoft SQL Server 2014 のコンポーネント:
<ul>
<li>データベース エンジン サービス</li>
<li>レポート サービス</li>
<li>分析サービス</li>
<li>Management Studio</li>
</ul></li>
</ul>
    <strong>注記:</strong> Reporting Services は、ネイティブモードで実行するようにコンフィギュレーションされています。 電源表示を使用するには、追加の構成手順を実行する必要があります。 詳細については、<a href="https://technet.microsoft.com/en-us/library/jj933492.aspx">キューブに接続するための Power View を使用したレポートの作成</a>に一覧表示された前提条件を参照してください。
<ul>
<li>AX 2012 R3 または AX 2012 R3 CU8 コンポーネント:
<ul>
<li>データベース</li>
<li>ビジネス インテリジェンス コンポーネント:
<ul>
<li>Reporting Services 拡張機能</li>
<li>Analysis Services の構成</li>
</ul></li>
</ul></li>
</ul></td>
</tr>
<tr class="odd">
<td>0</td>
<td>エンタープライズ ポータル サーバー</td>
<td><strong>サイズ:</strong>D3: 標準計算層 (4 コア、14 GB メモリ) <strong>既定名:</strong>EP-&lt;GUID&gt;</td>
<td><ul>
<li>Windows Server 2012 R2、以下を含む:
<ul>
<li>インターネット インフォメーション サービス (IIS)</li>
</ul></li>
<li>Microsoft SQL Server 2012 のコンポーネント:
<ul>
<li>フル テキスト検索</li>
</ul></li>
<li>Microsoft SharePoint Server 2013</li>
<li>AX 2012 R3 または AX 2012 R3 CU8 コンポーネント:
<ul>
<li>サーバー コンポーネント:
<ul>
<li>Web サーバー コンポーネント:
<ul>
<li>エンタープライズ ポータル (EP)</li>
<li>エンタープライズ検索</li>
<li>ヘルプ サーバー</li>
</ul></li>
</ul></li>
<li>Management Reporter コンポーネント:
<ul>
<li>Management Reporter サーバー コンポーネント</li>
</ul></li>
<li>小売コンポーネント:
<ul>
<li>Commerce Data Exchange コンポーネント:
<ul>
<li>Async Client</li>
</ul></li>
<li>Retail サーバー</li>
<li>小売オンライン チャネル</li>
<li>Retail チャンネル データベース</li>
<li>Retail チャンネル コンフィギュレーション ユーティリティ</li>
<li>Retail ハードウェア ステーション</li>
</ul></li>
<li>倉庫モバイル デバイス ポータル</li>
<li>Microsoft Dynamics Connector</li>
</ul></li>
</ul></td>
</tr>
<tr class="even">
<td>1</td>
<td>クライアント コンピューター</td>
<td><strong>サイズ:</strong>D3: 標準計算層 (4 コア、14 GB メモリ) <strong>既定名:</strong>CLI-&lt;GUID&gt;</td>
<td><ul>
<li>Windows Server 2012 R2</li>
<li>Microsoft Visual Studio 2013</li>
<li>Microsoft SQL Server 2014 のコンポーネント:
<ul>
<li>開発者ツール</li>
</ul></li>
<li>Microsoft SharePoint Server 2013 クライアント コンポーネント SDK</li>
<li>Microsoft Office 365 ProPlus</li>
<li>AX 2012 R3 または AX 2012 R3 CU8 コンポーネント:
<ul>
<li>Management Reporter コンポーネント:
<ul>
<li>Management Reporter レポート デザイナー</li>
</ul></li>
<li>クライアント コンポーネント:
<ul>
<li>クライアント</li>
<li>Office アドイン</li>
<li>リモート デスクトップ サービス統合</li>
</ul></li>
<li>開発者ツール:
<ul>
<li>デバッガー</li>
<li>Visual Studio Tools</li>
<li>Trace Parser</li>
</ul></li>
<li>管理ユーティリティ</li>
<li>小売コンポーネント:
<ul>
<li>Retail POS</li>
</ul></li>
</ul></li>
</ul></td>
</tr>
<tr class="odd">
<td>0</td>
<td>リモート デスクトップ サービス サーバー</td>
<td><strong>サイズ:</strong>D3: 標準計算層 (4 コア、14 GB メモリ) <strong>既定名:</strong>RDS-&lt;GUID&gt;</td>
<td><ul>
<li>Windows Server 2012 R2、以下を含む:
<ul>
<li>インターネット インフォメーション サービス (IIS)</li>
<li>リモート デスクトップ サービス</li>
</ul></li>
<li>Microsoft SQL Server 2012 Native Client</li>
</ul></td>
</tr>
</tbody>
</table>



## <a name="retail-essentials-devtest-environment"></a>Retail Essentials 開発/テスト環境
この環境を配置して、Retail essentials の機能を開発またはテストします。 この環境には、既定で 1 台の仮想マシンが含まれます。 この仮想マシンには、Windows Server と、Retail Essentials の開発とテストの目的で必要となるソフトウェアが既にインストールされています。 次のテーブルは、既定の Retail Essentials 開発/テスト環境の詳細を示しています。 環境を配置するとき、環境に追加の仮想マシンを追加する、または仮想マシンのサイズを変更することができます。 

> [!NOTE]
> この環境の仮想マシンは、単一インスタンスの仮想マシンです。 シングル インスタンス仮想マシンは、Azure [サービス レベル アグリーメント](http://azure.microsoft.com/en-us/support/legal/sla/)の対象となりません。

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<tbody>
<tr class="odd">
<td><strong>既定で配置される仮想マシンの数</strong></td>
<td><strong>説明</strong></td>
<td><strong>サイズと名前</strong></td>
<td><strong>ソフトウェア インストール済み</strong></td>
</tr>
<tr class="even">
<td>1</td>
<td>Retail Essentials サーバー</td>
<td><strong>サイズ:</strong>D3: 標準計算層 (4 コア、14 GB メモリ) <strong>既定名:</strong>ESSEN-&lt;GUID&gt;</td>
<td><ul>
<li>Windows Server 2012 R2</li>
<li>Microsoft SQL Server 2014 のコンポーネント:
<ul>
<li>データベース エンジン サービス</li>
<li>Management Studio</li>
<li>開発者ツール</li>
</ul></li>
<li>AX 2012 R3 コンポーネント:
<ul>
<li>データベース</li>
<li>サーバー コンポーネント:
<ul>
<li>Application Object Server (AOS)</li>
</ul></li>
<li>クライアント コンポーネント:
<ul>
<li>クライアント</li>
</ul></li>
<li>統合コンポーネント:
<ul>
<li>.NET Business Connector</li>
</ul></li>
<li>小売コンポーネント:
<ul>
<li>Retail Headquarters</li>
<li>Commerce Data Exchange コンポーネント:
<ul>
<li>Real-time Service</li>
<li>Async Server</li>
<li>Async Client</li>
</ul></li>
<li>Retail チャンネル データベース</li>
</ul></li>
</ul></li>
</ul></td>
</tr>
</tbody>
</table>



## <a name="retail-ecommerce-devtest-environment"></a>Retail E-commerce 開発/テスト環境
この環境を導入して、AX 2012 R3 と完全に統合されたオンライン販売チャネルを作成し、テストします。 この環境には、既定で 1 台の仮想マシンが含まれます。 この仮想マシンには、Windows Server と、小売電子商取引に必要なソフトウェアが既にインストールされています。 次のテーブルは、既定の Retail E-commerce 開発/テスト環境の詳細を示しています。 環境を配置するとき、環境に追加の仮想マシンを追加する、または仮想マシンのサイズを変更することができます。 

> [!NOTE]
> この環境の仮想マシンは、単一インスタンスの仮想マシンです。 シングル インスタンス仮想マシンは、Azure [サービス レベル アグリーメント](http://azure.microsoft.com/en-us/support/legal/sla/)の対象となりません。

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<tbody>
<tr class="odd">
<td><strong>既定で配置される仮想マシンの数</strong></td>
<td><strong>説明</strong></td>
<td><strong>サイズと名前</strong></td>
<td><strong>ソフトウェア インストール済み</strong></td>
</tr>
<tr class="even">
<td>1</td>
<td>Retail E-commerce サーバー</td>
<td><strong>サイズ:</strong>D3: 標準計算層 (4 コア、14 GB メモリ) <strong>既定名:</strong>E-COM-&lt;GUID&gt;</td>
<td><ul>
<li>Windows Server 2012 R2</li>
<li>Microsoft SharePoint Server 2013</li>
<li>AX 2012 R3 コンポーネント:
<ul>
<li>小売コンポーネント:
<ul>
<li>Commerce Data Exchange コンポーネント:
<ul>
<li>Async Client</li>
</ul></li>
<li>小売オンライン チャネル</li>
<li>Retail チャンネル データベース</li>
</ul></li>
</ul></li>
</ul></td>
</tr>
</tbody>
</table>

## <a name="retail-mobility-devtest-environment"></a>Retail mobility 開発/テスト環境
この環境を配置することで、販売スタッフが販売トランザクションを処理し、顧客注文を入力し、店舗内のどこでもモバイル デバイスを使用して日々の操作と在庫管理を実行できます。 この環境には、既定で 1 台の仮想マシンが含まれます。 この仮想マシンには、Windows Server と、小売モビリティに必要なソフトウェアが既にインストールされています。 次のテーブルは、既定の Retail Mobility 開発/テスト環境の詳細を示しています。 環境を配置するとき、環境に追加の仮想マシンを追加する、または仮想マシンのサイズを変更することができます。 
> [!NOTE]
> この環境の仮想マシンは、単一インスタンスの仮想マシンです。 シングル インスタンス仮想マシンは、Azure [サービス レベル アグリーメント](http://azure.microsoft.com/en-us/support/legal/sla/)の対象となりません。

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<tbody>
<tr class="odd">
<td><strong>既定で配置される仮想マシンの数</strong></td>
<td><strong>説明</strong></td>
<td><strong>サイズと名前</strong></td>
<td><strong>ソフトウェア インストール済み</strong></td>
</tr>
<tr class="even">
<td>1</td>
<td>Retail サーバー</td>
<td><strong>サイズ:</strong>D3: 標準計算層 (4 コア、14 GB メモリ) <strong>既定名:</strong>MOBIL-&lt;GUID&gt;</td>
<td><ul>
<li>Windows Server 2012 R2</li>
<li>AX 2012 R3 コンポーネント:
<ul>
<li>小売コンポーネント:
<ul>
<li>Commerce Data Exchange コンポーネント:
<ul>
<li>Async Client</li>
</ul></li>
<li>Retail サーバー</li>
<li>Retail チャンネル データベース</li>
</ul></li>
</ul></li>
</ul></td>
</tr>
</tbody>
</table>



## <a name="high-availability-environment"></a>高可用性環境
この環境を配置して、高可用性のために構成できる環境で AX 2012 R3 を使用します。 この環境には、数台の仮想マシンが含まれます。 これらの仮想マシンには、すでにインストールされている Windows Server および AX 2012 R3 を使用するために必要なソフトウェアがあります。 次のテーブルは、既定の高可用性環境の詳細を示しています。 環境を配置するとき、環境に追加の仮想マシンを追加する、または仮想マシンのサイズを変更することができます。 

> [!NOTE]
> Azure Premium Storage は高可用性環境が必要です。 詳細については、[Azure での高可用性環境の配置](deploy-high-availability-environment-azure.md) を参照してください。 この環境の仮想マシンは、Azure [サービス レベル アグリーメント](http://azure.microsoft.com/en-us/support/legal/sla/)の対象となります。 データのインポート/エクスポート フレームワーク (DIXF) コンポーネントは既定ではインストールされていません。 DIXF を使用する場合は、独自の SQL Server インストール メディアを使用して、SQL Server マシンに SQL Server Integration Services (SSIS) をインストールする必要があります。 SSIS をインストールした後は、Dynamics AX CD (VM 内の接続されたドライブで利用可能) を使用し、DIXF コンポーネントを AOS およびクライアント マシンにインストールできます。

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<tbody>
<tr class="odd">
<td><strong>既定で配置される仮想マシンの数</strong></td>
<td><strong>説明</strong></td>
<td><strong>サイズと名前</strong></td>
<td><strong>ソフトウェア インストール済み</strong></td>
</tr>
<tr class="even">
<td>3 <strong>注記:</strong> 3 つのドメイン コントローラがこの環境に配置されています。 1 つのドメイン コントローラーが失敗すると、Azure の<a href="http://azure.microsoft.com/en-us/support/legal/sla/">サービス レベル同意書</a>に準拠するために、2 つのオンライン ドメイン コントローラーを残しておく必要があります。</td>
<td>ドメイン コントローラー</td>
<td><strong>サイズ:</strong>D1: 基本的な計算層 (1 コア、3.5 GB メモリ) <strong>既定名:</strong>AD-&lt;GUID&gt;</td>
<td><ul>
<li>Windows Server 2012 R2、以下を含む:
<ul>
<li>Active Directory</li>
<li>ドメイン名サービス (DNS)</li>
</ul></li>
</ul></td>
</tr>
<tr class="odd">
<td>2</td>
<td>AOS サーバー</td>
<td><strong>サイズ:</strong>D3: 標準計算層 (4 コア、14 GB メモリ) <strong>既定名:</strong>AOS-&lt;GUID&gt;</td>
<td><ul>
<li>Windows Server 2012 R2、以下を含む:
<ul>
<li>インターネット インフォメーション サービス (IIS)</li>
</ul></li>
<li>Microsoft Visual Studio 2013</li>
<li>Microsoft Project Server</li>
<li>Microsoft SQL Server 2014 のコンポーネント:
<ul>
<li>Management Studio</li>
<li>ネイティブ クライアント</li>
</ul></li>
<li>AX 2012 R3 または AX 2012 R3 CU8 コンポーネント:
<ul>
<li>サーバー コンポーネント:
<ul>
<li>Application Object Server (AOS)</li>
</ul></li>
<li>クライアント コンポーネント:
<ul>
<li>クライアント</li>
<li>Office アドイン</li>
<li>リモート デスクトップ サービス統合</li>
</ul></li>
<li>統合コンポーネント:
<ul>
<li>IIS 上の Web サービス</li>
<li>.NET Business Connector</li>
</ul></li>
<li>管理ユーティリティ</li>
<li>小売コンポーネント:
<ul>
<li>Retail Headquarters</li>
<li>Commerce Data Exchange コンポーネント:
<ul>
<li>Synch Service</li>
<li>Real-time Service</li>
<li>Async Server</li>
</ul></li>
</ul></li>
<li>RapidStart Connector</li>
</ul></li>
</ul></td>
</tr>
<tr class="even">
<td>2</td>
<td>データベース サーバー</td>
<td><strong>サイズ:</strong>D3: 標準計算層 (4 コア、14 GB メモリ) <strong>既定名:</strong>SQL-&lt;GUID&gt;</td>
<td><ul>
<li>Windows Server 2012 R2</li>
<li>Microsoft SQL Server 2014 のコンポーネント:
<ul>
<li>データベース エンジン サービス</li>
<li>Management Studio</li>
</ul></li>
</ul>
<table>
<tbody>
<tr class="odd">
<td><strong>メモ</strong></td>
</tr>
<tr class="even">
<td>クォーラム サーバーも配置されます。 この仮想マシンは、AlwaysOn 可用性グループのリスナーです。 この仮想マシンは、o    [高可用性 VM] ボックスの一覧には表示されませんが、高可用性環境で展開されます。o    QRM -&lt;GUID&gt; という名前です。 この名前は customized.o にはできません    A2 仮想マシン.o です    Windows Server 2012 R2.o 配置後のギャラリー 画像を実行します。この VM は、高可用性環境に VM を追加するときに「データベース サーバー」として表示されます。 ここで参照されている 3 番目の VM は、明示的に SQL Server ではない A2 Quorum Server です。</td>
</tr>
<tr class="odd">
<td><strong>メモ</strong></td>
</tr>
<tr class="even">
<td>Reporting Services は、ネイティブモードで実行するようにコンフィギュレーションされています。 電源表示を使用するには、追加の構成手順を実行する必要があります。 詳細については、<a href="https://technet.microsoft.com/en-us/library/jj933492.aspx">キューブに接続するための Power View を使用したレポートの作成</a>に一覧表示された前提条件を参照してください。</td>
</tr>
</tbody>
</table>
<ul>
<li>AX 2012 R3 または AX 2012 R3 CU8 コンポーネント:
<ul>
<li>データベース</li>
</ul></li>
</ul></td>
</tr>
<tr class="odd">
<td>2</td>
<td>ビジネス インテリジェンス (BI) サーバー</td>
<td><strong>サイズ:</strong>D3: 標準計算層 (4 コア、14 GB メモリ) <strong>既定名:</strong>BI-&lt;GUID&gt;</td>
<td><ul>
<li>Windows Server 2012 R2</li>
<li>Microsoft SQL Server 2014 のコンポーネント:
<ul>
<li>データベース エンジン サービス</li>
<li>レポート サービス</li>
<li>分析サービス</li>
<li>Management Studio</li>
</ul></li>
</ul>
<table>
<tbody>
<tr class="odd">
<td><strong>メモ</strong></td>
</tr>
<tr class="even">
<td>Reporting Services は、ネイティブモードで実行するようにコンフィギュレーションされています。 電源表示を使用するには、追加の構成手順を実行する必要があります。 詳細については、<a href="https://technet.microsoft.com/en-us/library/jj933492.aspx">キューブに接続するための Power View を使用したレポートの作成</a>に一覧表示された前提条件を参照してください。</td>
</tr>
</tbody>
</table>
<ul>
<li>AX 2012 R3 または AX 2012 R3 CU8 コンポーネント:
<ul>
<li>ビジネス インテリジェンス コンポーネント:
<ul>
<li>Reporting Services 拡張機能</li>
<li>Analysis Services の構成</li>
</ul></li>
</ul></li>
</ul></td>
</tr>
<tr class="even">
<td>0</td>
<td>エンタープライズ ポータル サーバー</td>
<td><strong>サイズ:</strong>D3: 標準計算層 (4 コア、14 GB メモリ) <strong>既定名:</strong>EP-&lt;GUID&gt;</td>
<td><ul>
<li>Windows Server 2012 R2、以下を含む:
<ul>
<li>インターネット インフォメーション サービス (IIS)</li>
</ul></li>
<li>Microsoft SQL Server 2012 のコンポーネント:
<ul>
<li>フル テキスト検索</li>
</ul></li>
<li>Microsoft SharePoint Server 2013</li>
<li>AX 2012 R3 または AX 2012 R3 CU8 コンポーネント:
<ul>
<li>サーバー コンポーネント:
<ul>
<li>Web サーバー コンポーネント:
<ul>
<li>エンタープライズ ポータル (EP)</li>
<li>エンタープライズ検索</li>
<li>ヘルプ サーバー</li>
</ul></li>
</ul></li>
<li>Management Reporter コンポーネント:
<ul>
<li>Management Reporter サーバー コンポーネント</li>
</ul></li>
<li>小売コンポーネント:
<ul>
<li>Commerce Data Exchange コンポーネント:
<ul>
<li>Async Client</li>
</ul></li>
<li>Retail サーバー</li>
<li>小売オンライン チャネル</li>
<li>Retail チャンネル データベース</li>
<li>Retail チャンネル コンフィギュレーション ユーティリティ</li>
<li>Retail ハードウェア ステーション</li>
</ul></li>
<li>倉庫モバイル デバイス ポータル</li>
<li>Microsoft Dynamics Connector</li>
</ul></li>
</ul></td>
</tr>
<tr class="odd">
<td>2</td>
<td>クライアント コンピューター</td>
<td><strong>サイズ:</strong>D3: 標準計算層 (4 コア、14 GB メモリ) <strong>既定名:</strong>CLI-&lt;GUID&gt;</td>
<td><ul>
<li>Windows Server 2012 R2</li>
<li>Microsoft Visual Studio 2013</li>
<li>Microsoft SQL Server 2014 のコンポーネント:
<ul>
<li>開発者ツール</li>
</ul></li>
<li>Microsoft SharePoint Server 2013 クライアント コンポーネント SDK</li>
<li>Microsoft Office 365 ProPlus</li>
<li>AX 2012 R3 または AX 2012 R3 CU8 コンポーネント:
<ul>
<li>Management Reporter コンポーネント:
<ul>
<li>Management Reporter レポート デザイナー</li>
</ul></li>
<li>クライアント コンポーネント:
<ul>
<li>クライアント</li>
<li>Office アドイン</li>
<li>リモート デスクトップ サービス統合</li>
</ul></li>
<li>開発者ツール:
<ul>
<li>デバッガー</li>
<li>Visual Studio Tools</li>
<li>Trace Parser</li>
</ul></li>
<li>管理ユーティリティ</li>
<li>小売コンポーネント:
<ul>
<li>Retail POS</li>
</ul></li>
</ul></li>
</ul></td>
</tr>
<tr class="even">
<td>2</td>
<td>リモート デスクトップ サービス サーバー</td>
<td><strong>サイズ:</strong>D3: 標準計算層 (4 コア、14 GB メモリ) <strong>既定名:</strong>RDS-&lt;GUID&gt;</td>
<td><ul>
<li>Windows Server 2012 R2、以下を含む:
<ul>
<li>インターネット インフォメーション サービス (IIS)</li>
<li>リモート デスクトップ サービス</li>
</ul></li>
<li>Microsoft SQL Server 2012 Native Client</li>
</ul></td>
</tr>
</tbody>
</table>



## <a name="next-steps"></a>次のステップ
- [Azure に AX 2012 R3 または AX 2012 R3 CU8 デモ環境を配置する](deploy-ax-2012-r3-ax-2012-r3-cu8-demo-environment-azure.md) 
- [Azure での Retail Essentials デモ環境の配置](deploy-retail-essentials-demo-environment-azure.md) 
- [Azure での開発環境の配置](deploy-development-environment-azure.md) 
- [Azure でのテスト環境の配置](deploy-test-environment-azure.md) 
- [Azure での Retail Essentials 開発/テスト環境の配置](deploy-retail-essentials-devtest-environment-azure.md) 
- [Azure での Retail E-commerce 開発/テスト環境の配置](deploy-retail-ecommerce-devtest-environment-azure.md) 
- [Azure での Retail Mobility 開発/テスト環境の配置](deploy-retail-mobility-devtest-environment-azure.md) 
- [Azure に高可用性環境を配置する](deploy-high-availability-environment-azure.md)

