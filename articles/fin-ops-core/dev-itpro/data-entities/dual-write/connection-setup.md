---
title: デュアル書き込みの設定方法に関するガイダンス
description: この記事では、デュアル書き込みの設定でサポートされているシナリオについて説明します。
author: RamaKrishnamoorthy
ms.date: 10/12/2020
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: tfehr
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2020-01-06
ms.openlocfilehash: a0d1b4e1f093874a8fd37cf7aadb331cd1e7adc4
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/03/2022
ms.locfileid: "8873152"
---
# <a name="guidance-for-dual-write-setup"></a>デュアル書き込みの設定方法に関するガイダンス

[!include [banner](../../includes/banner.md)]

[!include [preview-banner](../../includes/preview-banner.md)]



Finance and Operations 環境と Dataverse 環境との間には、デュアル書き込み接続を設定できます。

+ **財務と運用環境** では、**財務と運用アプリ** の基盤となるプラットフォームを提供します (たとえば、Microsoft Microsoft Dynamics 365 Finance、Dynamics 365 Supply Chain Management、Dynamics 365 Commerce、Dynamics 365 Human Resources)。
+ **Dataverse 環境** では、**Customer Engagement アプリ** (Dynamics 365 Sales、Dynamics 365 Customer Service、Dynamics 365 column Service、Dynamics 365 Marketing、および Dynamics 365 Project Service Automation) の基盤となるプラットフォームを提供します。

> [!IMPORTANT]
> Dynamics 365 Finance の Human Resources モジュールでは 、デュアル書き込み接続に対応していますが、Dynamics 365 Human Resources アプリでは対応していません。

この設定のメカニズムは、サブスクリプションや環境によって異なります。

+ 財務と運用アプリの新しいインスタンスの場合、デュアル書き込み接続の設定は Microsoft Dynamics Lifecycle Services (LCS) で開始されます。 Microsoft Power Platform のライセンスを所有している際は、テナントに無い場合、新しい Dataverse 環境が得られます。
+ 財務と運用アプリの既存のインスタンスの場合、デュアル書き込み接続の設定は Finance and Operations 環境で開始されます。

エンティティでデュアル書き込みを開始する前に、最初の同期を実行して、財務と運用アプリと Customer Engagement アプリの両面で既存のデータを処理することができます。 2 つの環境間でデータを同期する必要がない場合は、初期同期を省略できます。

初期同期では、既存のデータをひとつのアプリから双方向の別のアプリにコピーできます。 設定のシナリオには、使用中の環境や環境に含まれるデータのタイプによって、さまざまなシナリオがあります。

サポートされている設定シナリオは次のとおりです。

+ [新しいの財務と運用アプリ インスタンスと新しい Customer Engagement アプリ インスタンス](#new-new)
+ [新しい財務と運用アプリ インスタンスと既存の Customer Engagement アプリ インスタンス](#new-existing)
+ [データを持つ新しい財務と運用アプリのインスタンスと、新しい Customer Engagement アプリ インスタンス](#new-data-new)
+ [データを持つ新しい財務と運用アプリのインスタンスと、既存の Customer Engagement アプリ インスタンス](#new-data-existing)
+ [既存の財務と運用アプリ インスタンスと新しい Customer Engagement アプリ インスタンス](#existing-new)
+ [既存の財務と運用アプリ インスタンスと既存の Customer Engagement アプリ インスタンス](#existing-existing)

## <a name="a-new-finance-and-operations-app-instance-and-a-new-customer-engagement-app-instance"></a><a id="new-new"></a>新しいの財務と運用アプリ インスタンスと新しい Customer Engagement アプリ インスタンス

データを持たない財務と運用アプリの新しいインスタンスと、Customer Engagement アプリの新しいインスタンスとの間でデュアル ライト接続を設定するには、 [Lifecycle Services からのデュアルライト設定](lcs-setup.md)の手順に従います。 接続の設定が完了すると、次のアクションが自動的に実行されます。

- 新しいブランクの Finance and Operations 環境がプロビジョニングされます。
- Customer Engagement アプリの新しい空のインスタンスがプロビジョニングされ、CRM の主要ソリューションがインストールされます。
- DAT 会社のデータに対して、デュアル書き込み接続が確立されます。
- テーブル マップでは、ライブ同期が有効になっています。

次に、両方の環境について、ライブ データ同期の準備が整います。

## <a name="a-new-finance-and-operations-app-instance-and-an-existing-customer-engagement-app-instance"></a><a id="new-existing"></a>新しい財務と運用アプリ インスタンスと既存の Customer Engagement アプリ インスタンス

データを持たない財務と運用アプリの新しいインスタンスと、Customer Engagement アプリの既存のインスタンスとの間でデュアル ライト接続を設定するには、 [Lifecycle Services からのデュアルライト設定](lcs-setup.md)の手順に従います。 接続の設定が完了すると、次のアクションが自動的に実行されます。

- 新しいブランクの Finance and Operations 環境がプロビジョニングされます。
- DAT 会社のデータに対して、デュアル書き込み接続が確立されます。
- テーブル マップでは、ライブ同期が有効になっています。

次に、両方の環境について、ライブ データ同期の準備が整います。

既存の Dataverse データを財務と運用アプリケーションに同期するには、次の手順に従います。

1. 財務と運用アプリで新しい会社を作成します。
2. デュアル書き込み接続の設定に会社を追加します。
3. 3 文字の国際標準化機構 (ISO) 会社コードを使用し、Dataverse データを [Bootstrap](bootstrap-company-data.md) にて実行します。
4. データを同期するテーブルの **初期同期** 機能を実行します。

例へのリンクや代替のアプローチについては、この記事で後述する[使用例](#example)のセクションを参照してください。

## <a name="a-new-finance-and-operations-app-instance-that-has-data-and-a-new-customer-engagement-app-instance"></a><a id="new-data-new"></a>データを持つ新しい財務と運用アプリのインスタンスと、新しい Customer Engagement アプリ インスタンス

データを持つ財務と運用アプリの新しいインスタンスと Customer Engagement アプリの新しいインスタンス間にデュアル書き込み接続を設定するには、この記事前半の[新しい財務と運用アプリ インスタンスと新しい Customer Engagement アプリ インスタンス](#new-new)セクションに記載の手順に従います。 接続の設定が完了したら、データを Customer Engagement アプリに同期する場合には、次の手順に従います。

1. LCS ページから財務と運用アプリを開き、ログインして、**データ管理 \> デュアル書き込み** の順に移動します。
2. データを同期するテーブルの **初期同期** 機能を実行します。

例へのリンクや代替のアプローチについては、[使用例](#example)のセクションを参照してください。

## <a name="a-new-finance-and-operations-app-instance-that-has-data-and-an-existing-customer-engagement-app-instance"></a><a id="new-data-existing"></a>データを持つ新しい財務と運用アプリのインスタンスと、既存の Customer Engagement アプリ インスタンス

データを持つ財務と運用アプリの既存のインスタンスと Customer Engagement アプリの新しいインスタンス間にデュアル書き込み接続を設定するには、この記事前半の[新しい財務と運用アプリ インスタンスと既存の Customer Engagement アプリ インスタンス](#new-existing)セクションに記載の手順に従います。 接続の設定が完了したら、データを Customer Engagement アプリに同期する場合には、次の手順に従います。

1. LCS ページから財務と運用アプリを開き、ログインして、**データ管理 \> デュアル書き込み** の順に移動します。
2. データを同期するテーブルの **初期同期** 機能を実行します。

既存の Dataverse データを財務と運用アプリケーションに同期するには、次の手順に従います。

1. 財務と運用アプリで新しい会社を作成します。
2. デュアル書き込み接続の設定に会社を追加します。
3. 3 文字の ISO 会社コードを使用し、Dataverse データを [Bootstrap](bootstrap-company-data.md) にて実行します。
4. データを同期するテーブルの **初期同期** 機能を実行します。

例へのリンクや代替のアプローチについては、[使用例](#example)のセクションを参照してください。

## <a name="an-existing-finance-and-operations-app-instance-and-a-new-customer-engagement-app-instance"></a><a id="existing-new"></a>既存の財務と運用アプリ インスタンスと新しい Customer Engagement アプリ インスタンス

財務と運用アプリの既存インスタンスと Customer Engagement アプリの新規のインスタンス間のデュアル書き込み接続の設定は、Finance and Operation 環境で発生します。

1. [財務と運用アプリからの接続設定](enable-dual-write.md)。
2. データを同期するテーブルの **初期同期** 機能を実行します。

例へのリンクや代替のアプローチについては、[使用例](#example)のセクションを参照してください。

## <a name="an-existing-finance-and-operations-app-instance-and-an-existing-customer-engagement-app-instance"></a><a id="existing-existing"></a>既存の財務と運用アプリ インスタンスと既存の Customer Engagement アプリ インスタンス

財務と運用アプリの既存インスタンスと Customer Engagement アプリの既存のインスタンス間のデュアル書き込み接続の設定は、Finance and Operation 環境で発生します。

1. [財務と運用アプリからの接続設定](enable-dual-write.md)。
2. 既存の Dataverse データを財務と運用アプリに同期するには、3 文字の ISO 会社コードを使用して、Dataverse データを [ブートストラップ](bootstrap-company-data.md) にて実行します。
3. データを同期するテーブルの **初期同期** 機能を実行します。

例へのリンクや代替のアプローチについては、[使用例](#example)のセクションを参照してください。

## <a name="example"></a>例

例については、[Customers V3 の有効化—連絡先テーブル マップ](enable-entity-map.md#enable-table-map)を参照してください

初期同期を実行する必要がある各エンティティのデータ ボリュームに基づく代替的なアプローチについては、[初期同期の考慮事項](initial-sync-guidance.md)を参照してください。


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]