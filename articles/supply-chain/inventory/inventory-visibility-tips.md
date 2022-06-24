---
title: Inventory Visibility のヒント
description: この記事では、在庫可視化アドインを設定して使用する際に役立つヒントを紹介します。
author: yufeihuang
ms.date: 08/02/2021
ms.topic: article
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yufeihuang
ms.search.validFrom: 2021-08-02
ms.dyn365.ops.version: 10.0.21
ms.openlocfilehash: 9f571d353f99c91776424bc2fa3405f73b2bae0a
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/03/2022
ms.locfileid: "8885960"
---
# <a name="inventory-visibility-tips"></a>在庫可視化のヒント

[!include [banner](../includes/banner.md)]

ここでは、在庫可視化アドインをセットアップして使用する際に考慮すべきいくつかのヒントをご紹介します:

- 現在、在庫可視化アドインは、Microsoft Dynamics Lifecycle Services (LCS) を使用して作成された Microsoft Dataverse 環境のみをサポートしています。 Dataverse 環境が他の方法で作成され (例: Power Apps 管理センターを使用)、それが Dynamics 365 Supply Chain Management 環境にリンクされている場合は、在庫可視化製品チームにマッピングの問題を修正してもらう必要があります。 チームには、[inventvisibilitysupp@microsoft.com](mailto:inventvisibilitysupp@microsoft.com) までご連絡ください。 ご利用の環境に在庫可視化をインストールする準備ができたら、チームからお知らせします。
- 複数の LCS 環境を使用する場合は、環境ごとに異なる Azure Active Directory (Azure AD) アプリケーションを作成します。 同じアプリケーション ID とテナント ID を使用して異なる環境の在庫視覚化アドインをインストールした場合、古い環境ではトークンの問題が発生します。 最後にインストールされた在庫可視化アドインのインスタンスのみが有効になります。
- 在庫の可視性は、現在、クラウド ホスト環境ではサポートされていません。 これは、Tier-2+ 環境でのみサポートされます。
- アプリケーション プログラミング インターフェース (API) は、現在、最大 100 個の個別項目を `ProductID` の値で照会することをサポートしています。 各クエリには、複数の `SiteID` と `LocationID` の値を指定することもできます。 最大制限は、`NumOf(SiteID) * NumOf(LocationID) <= 100` として定義されます。
- バルク API では、要求ごとに最大 512 件のレコードを返します。
- `fno` データ ソースは Supply Chain Management 用に予約されています。 在庫可視性アドインが Supply Chain Management 環境と統合されている場合は、[データソース](inventory-visibility-configuration.md#data-source-configuration)の `fno` に関連する設定を削除しないことをお勧めします。
- 在庫品目一覧で `fno` データ ソースのデータを変更できない。 データ フローは一方向です。つまり、`fno` データ ソースに対するすべての数量の変更は、Supply Chain Management 環境から取得される必要があります。 したがって、API を使用して `fno` データ ソースに対する受信要求や引当要求を送信することはできません。
- Supply Chain Management 環境に 1 つ以上の新しいメジャーを追加する場合は、在庫の可視性にも追加する必要があります。 ただし、新しいメジャーの数量変更はすべて Supply Chain Management 環境から行う必要があります。
- 現在、[パーティション構成](inventory-visibility-configuration.md#partition-configuration)は、データの分散方法を示す 2 つの基本分析コード (`SiteId` と `LocationId`) で構成されています。 同じパーティションで運用することで、より高いパフォーマンスを低コストで実現できます。 ソリューションには、このパーティション構成が規定で含まれています。 したがって、 *自分で定義する必要はありません*。 既定のパーティション構成をカスタマイズしないでください。 それを削除したり変更したりすると、予期せぬエラーが発生する可能性があります。
- パーティション構成で定義されている基本分析コードは、[プロダクトインデックスの階層構成](inventory-visibility-configuration.md#index-configuration) では定義しないでください。
- [製品インデックス階層構成](inventory-visibility-configuration.md#index-configuration) には、少なくとも 1 つのインデックス階層 (基準分析コード `Empty` を含むなど) を含める必要があります。そうしない場合、クエリは "インデックス階層が設定されていません" というエラーで失敗します。

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
