---
title: Power BI Embedded 統合
description: この記事では、Power BI Embedded 統合を使用するための方法について説明します。
author: RichdiMSFT
ms.date: 02/09/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Developer, IT Pro
ms.reviewer: sericks
ms.search.region: Global
ms.author: richdi
ms.search.validFrom: 2017-02-28
ms.dyn365.ops.version: Platform update 4
ms.custom:
- "270754"
ms.assetid: ca4b2ccf-d68d-4344-833e-1c45d966246c
ms.openlocfilehash: 557271df3a2255840bbce74a9b7b17b09c180972
ms.sourcegitcommit: 3c4dd125ed321af8a983e89bcb5bd6e5ed04a762
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/28/2022
ms.locfileid: "9206599"
---
# <a name="power-bi-embedded-integration"></a>Power BI Embedded 統合

[!include [banner](../includes/banner.md)]

パートナーおよび独立系ソフトウェア ベンダー (ISV) が開発した Microsoft Power BI コンテンツは、Microsoft Dynamics 365 Finance に直接埋め込むことができます。 この記事では、Microsoft Power BI Embedded 統合を使用するための方法について説明します。

## <a name="overview"></a>概要
アプリケーションと [Power BI](https://www.powerbi.com/) の統合により、Microsoft Power Query for Excel でサポートされている外部データ ソースへのアクセスが必要なデータ マッシュアップ シナリオが可能になります。 ユーザーは、PowerBI.com でホストされているタイルを埋め込むことにより、ワークスペースをカスタマイズできます。 ユーザーは、PowerBI.com でホストされているレポートに直接リンクを追加することもできます。 このようにして、ユーザーはアプリケーションを終了せずにレポートにアクセスし、対話できます。 パートナーと ISV が開発する Power BI コンテンツ (PBIX ファイル) は、アプリケーションに直接埋め込むことができます。 モデル ファイルに関連付けられている PBIX ファイルは、アプリケーション配置プロセスの一部として Power BI Embedded で自動的に公開されます。 また、次の機能が必要な埋め込みレポート シナリオの X++ 拡張機能を追加できます。

- ユーザー インタラクションに応じた詳細ページへナビゲーションをドリルダウン
- 会社または日付の範囲など、ユーザーとセッション コンテキスト情報に基づいたレポート フィルター
- Power BI レポートの特定のタブにメニュー項目から直接移動する機能

拡張機能を使用するカスタマイズに関する詳細については、 [拡張機能およびオーバーレイによるカスタマイズ](../extensibility/customization-overlayering-extensions.md) を参照してください。

## <a name="advantages-of-power-bi-embedded"></a>Power BI Embedded のメリット
- **アプリケーションで Power BI ワークスペースとレポートを配信します。** ユーザーが power user またはビジネス アナリストである場合は、Power BI ツールを使用して既製のレポートを調整したり、新しいレポートを作成することができます。 開発者は、ワークスペースを通じて製品の豊富なナビゲーション エクスペリエンスを提供するためにユーザーが作成したレポートを使用できます。 パートナーおよび ISV コミュニティにいる場合は、Power BI エクスペリエンスを含む豊富なワークスペースを構築し、そのワークスペースをソリューションの一部としてリリースすることができます。
- **Power BI Embedded サービス ライセンスは、アプリケーションにまとめられます。** ユーザーが ISV またはシステム インテグレーターである場合は、Microsoft Dynamics Lifecycle Services (LCS) ソリューションの一部として、Power BI で有効化されたワークスペース (およびこれらのワークスペースにより提供されるナビゲーション エクスペリエンス) をパッケージ化できます。 顧客は、PowerBI.com サブスクリプションなしで、同じ体験をします。 ワークスペースは、財務と運用アプリケーションで動作します。
- **Power BI から詳細ページへのドリルダウンを有効にします。** ビジュアルは、アクションの開始点です。 ユーザーは、業務プロセスやページにドリルダウンして、明らかになっていない問題にすぐ対応できます。 ユーザーは、ビジュアルを使用して、データをフィルタリングして傾向を把握できます。 アクションのページには、注意が必要なデータのセットのみを反映します。
- **メニュー項目を使用して Power BI レポートへのアクセスを保護します。** 開発者は、Power BI の基準となるワークスペースに同一の概念を拡張するために、財務と運用アプリで利用可能な使い慣れたプログラミングの概念を使用できます。 Power BI で駆動される概要ページを追加することにより、ワークスペースを新規作成または既存のワークスペースを拡張することができます。 開発者は、メニュー項目を Power BI レポートに関連付けて、リンクをワークスペースに含めることができます。 財務と運用アプリにおけるロール ベースおよびタスク ベースのセキュリティは、これらのメニュー項目を保護するために使用できます。
- **アプリケーション コンテキストに基づくレポートのフィルター処理。** 1 つまたは複数のフィルターを Power BI レポートに渡すことにより、ナビゲーション エクスペリエンスをビルドすることができます。 たとえば、ユーザーのアクションまたはコンテキストに応じて、Power BI レポートが 1 つの事業単位または特定の製品からのデータを反映するようにフィルタ処理できます。 ユーザーはデータをフィルタリングする必要はありません。 ユーザーがトランザクション詳細ページに直接移動することができる、財務と運用ページへのドリルスルー リンクを定義することができます。

Power BI Embedded サービスの詳細については、「[Power BI FAQ](https://powerbi.microsoft.com/documentation/powerbi-frequently-asked-questions/)」を参照してください。

## <a name="service-availability"></a>サービスの可用性
**Power BI Embedded サービスは自動的に配置し、すべてのクラウド ホスト、複数のボックス配置を構成します。** このサービスは Microsoft Azure サービスに依存しているため、アプリケーションの分析ワークスペースとレポートはワンボックス環境では使用できません。 Power BI Embedded サービスは、ほとんどの Azure データ センターで既に利用できます。 [Azure の状態](https://azure.microsoft.com/status/) ページで最新の使用可能性を確認することができます。

## <a name="frequently-asked-questions"></a>よく寄せられる質問

### <a name="can-i-customize-the-power-bi-embedded-reports"></a>Power BI の埋め込まれたレポートをカスタマイズすることはできますか。
はい。 Power BI Embedded レポートをカスタマイズするには、 Power BI Desktop をワンボックス環境にインストールし、 [Power BI Desktop を使用した分析レポートの作成](author-distribute-power-bi-reports.md) の手順に従います。
 
### <a name="do-customers-have-to-purchase-a-separate-power-bi-license-to-use-the-new-embedded-analytics"></a>顧客は、新しい埋め込み分析を使用する個別 Power BI ライセンスを購入する必要があるか。
いいえ、顧客は、新しい埋め込み分析を使用する個別 Power BI ライセンスを購入する必要はありません。 ただし、DirectQuery を使用して PowerBI.com からエンティティ ストアに接続するためには Power BI Pro ライセンスが必要です。
 
### <a name="can-i-do-data-mash-ups-by-using-external-data-in-the-embedded-reports"></a>埋め込まれたレポートで外部データを使用してデータのマッシュアップを実行できますか。
いいえ、現在埋め込まれたレポートで外部データを使用してデータのマッシュアップを実行できません。
 
### <a name="can-i-help-secure-data-to-only-those-companies-that-i-have-access-to"></a>私がアクセスしているこれらの会社にのみデータを保護することはできますか。
はい、単一の会社ビューではアクセス権を持たない会社からデータにアクセスすることはできません。 カスタム ソリューションをセキュリティで保護する方法の詳細については、「[Power BI Embedded を使用して分析ワークスペースおよびレポートをセキュリティで保護](secure-analytical-workspaces.md)」を参照してください。
 
### <a name="how-is-currency-shown-across-multiple-companies"></a>通貨は複数の会社間でどのように表示されますか。
通貨は、システム通貨で示されます。 システム通貨は、**システム パラメーター** ページで定義されます。
 
### <a name="can-i-drill-from-summary-balances-back-into-finance-and-operations"></a>財務と運用に戻す概要残高をドリルすることはできますか?
はい、Power BI レポートの詳細を表示することができます。 ただし、財務と運用アプリへのドリルダウンに対するサポートは限られています。
 
### <a name="what-languages-are-currently-supported"></a>現在どのような言語がサポートされていますか。
現在、英語のみがサポートされています。 ただし、Power BI チームはその他の言語のサポートを追加する予定です。
 
### <a name="can-i-access-analytical-workspaces-and-reports-in-the-on-premises-version-of-finance-and-operations"></a>財務と運用のオンプレミス バージョンで分析ワークスペースおよびレポートにアクセスすることはできますか?
いいえ、現在は Dynamics 365 Finance + Operations (on-premises) の分析ワークスペースおよびレポートにアクセスできません。 インテリジェンス機能のシステムは、クラウドにホストされているソリューションに依存します。


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
