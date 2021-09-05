---
title: デュアル書き込みの設定方法に関するガイダンス
description: このトピックでは、デュアル書き込みの設定でサポートされているシナリオについて説明します。
author: RamaKrishnamoorthy
ms.date: 10/12/2020
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2020-01-06
ms.openlocfilehash: 6450ef7b0a59df3a8da2c8bed3aa9c0b14a9cc97
ms.sourcegitcommit: 259ba130450d8a6d93a65685c22c7eb411982c92
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/24/2021
ms.locfileid: "7417060"
---
# <a name="guidance-for-dual-write-setup"></a>デュアル書き込みの設定方法に関するガイダンス

[!include [banner](../../includes/banner.md)]

[!include [preview-banner](../../includes/preview-banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Finance and Operations 環境と Dataverse 環境との間には、デュアル書き込み接続を設定できます。

+ **Finance and Operations 環境** では、**Finance and Operations アプリケーション** の基盤となるプラットフォームを提供します (たとえば、Microsoft Dynamics 365 Finance、Dynamics 365 Supply Chain Management、Dynamics 365 Commerce、および Dynamics 365 Human Resources)。
+ **Dataverse 環境** では、**Customer Engagement アプリ** (Dynamics 365 Sales、Dynamics 365 Customer Service、Dynamics 365 column Service、Dynamics 365 Marketing、および Dynamics 365 Project Service Automation) の基盤となるプラットフォームを提供します。

> [!IMPORTANT]
> Dynamics 365 Finance の Human Resources モジュールでは 、デュアル書き込み接続に対応していますが、Dynamics 365 Human Resources アプリでは対応していません。

この設定のメカニズムは、サブスクリプションや環境によって異なります。

+ Finance and Operations アプリの新しいインスタンスの場合、デュアル書き込み接続の設定は Microsoft Dynamics Lifecycle Services (LCS) で開始されます。 Microsoft Power Platform のライセンスを所有している際は、テナントに無い場合、新しい Dataverse 環境が得られます。
+ 既存のインスタンス Finance and Operations アプリの場合、デュアル書き込み接続の設定は Finance and Operations環境で開始されます。

エンティティでデュアル書き込みを開始する前に、最初の同期を実行して、Finance and Operations アプリと Customer Engagement アプリの両面で既存のデータを処理することができます。 2 つの環境間でデータを同期する必要がない場合は、初期同期を省略できます。

初期同期では、既存のデータをひとつのアプリから双方向の別のアプリにコピーできます。 設定のシナリオには、使用中の環境や環境に含まれるデータのタイプによって、さまざまなシナリオがあります。

サポートされている設定シナリオは次のとおりです。

+ [新しい Finance and Operations アプリ インスタンスと新しい Customer Engagement アプリ インスタンス](#new-new)
+ [新しい Finance and Operations アプリ インスタンスと既存の Customer Engagement アプリ インスタンス](#new-existing)
+ [データ付き新しい Finance and Operations アプリ インスタンスと新しい Customer Engagement アプリ インスタンス](#new-data-new)
+ [データ付き新しい Finance and Operations アプリ インスタンスと既存の Customer Engagement アプリ インスタンス](#new-data-existing)
+ [既存の Finance and Operations アプリ インスタンスと新しい Customer Engagement アプリ インスタンス](#existing-new)
+ [既存の Finance and Operations アプリ インスタンスと既存の Customer Engagement アプリ インスタンス](#existing-existing)

## <a name="a-new-finance-and-operations-app-instance-and-a-new-customer-engagement-app-instance"></a><a id="new-new"></a>新しい Finance and Operations アプリ インスタンスと新しい Customer Engagement アプリ インスタンス

データ無しの Finance and Operations アプリの新しいインスタンスと Customer Engagement アプリの新しいインスタンス間のデュアル書き込み接続を設定するには、[Lifecycle Services からのデュアル書き込み設定](lcs-setup.md) の手順に従います。 接続の設定が完了すると、次のアクションが自動的に実行されます。

- 新しい空の Finance and Operations 環境が準備されます。
- Customer Engagement アプリの新しい空のインスタンスがプロビジョニングされ、CRM の主要ソリューションがインストールされます。
- DAT 会社のデータに対して、デュアル書き込み接続が確立されます。
- テーブル マップでは、ライブ同期が有効になっています。

次に、両方の環境について、ライブ データ同期の準備が整います。

## <a name="a-new-finance-and-operations-app-instance-and-an-existing-customer-engagement-app-instance"></a><a id="new-existing"></a>新しい Finance and Operations アプリ インスタンスと既存の Customer Engagement アプリ インスタンス

データ無しの Finance and Operations アプリの新しいインスタンスと Customer Engagement アプリの既存のインスタンス間のデュアル書き込み接続を設定するには、[Lifecycle Services からのデュアル書き込み設定](lcs-setup.md) の手順に従います。 接続の設定が完了すると、次のアクションが自動的に実行されます。

- 新しい空の Finance and Operations 環境が準備されます。
- DAT 会社のデータに対して、デュアル書き込み接続が確立されます。
- テーブル マップでは、ライブ同期が有効になっています。

次に、両方の環境について、ライブ データ同期の準備が整います。

既存の Dataverse データを Finance and Operations アプリに同期するには、次の手順に従います。

1. Finance and Operations アプリに新しい会社を作成します。
2. デュアル書き込み接続の設定に会社を追加します。
3. 3 文字の国際標準化機構 (ISO) 会社コードを使用し、Dataverse データを [Bootstrap](bootstrap-company-data.md) にて実行します。
4. データを同期するテーブルの **初期同期** 機能を実行します。

例へのリンクや代替のアプローチについては、このトピックで後述する[使用例](#example)のセクションを参照してください。

## <a name="a-new-finance-and-operations-app-instance-that-has-data-and-a-new-customer-engagement-app-instance"></a><a id="new-data-new"></a>データ付き新しい Finance and Operations アプリ インスタンスと新しい Customer Engagement アプリ インスタンス

データ付き Finance and Operations アプリの新しいインスタンスと Customer Engagement アプリの新しいインスタンス間にデュアル書き込み接続を設定するには、このトピック前半の[新しい Finance and Operations アプリ インスタンスと新しい Customer Engagement アプリ インスタンス](#new-new) セクションにある手順に従います。 接続の設定が完了したら、データを Customer Engagement アプリに同期する場合には、次の手順に従います。

1. LCS ページから Finance and Operations アプリを開き、ログインして、**データ管理 \> デュアル書き込み** の順に移動します。
2. データを同期するテーブルの **初期同期** 機能を実行します。

例へのリンクや代替のアプローチについては、[使用例](#example)のセクションを参照してください。

## <a name="a-new-finance-and-operations-app-instance-that-has-data-and-an-existing-customer-engagement-app-instance"></a><a id="new-data-existing"></a>データ付き新しい Finance and Operations アプリ インスタンスと既存の Customer Engagement アプリ インスタンス

データ付き Finance and Operations アプリの新しいインスタンスと Customer Engagement アプリの既存のインスタンス間にデュアル書き込み接続を設定するには、このトピック前半の[新しい Finance and Operations アプリ インスタンスと既存の Customer Engagement アプリ インスタンス](#new-existing) セクションにある手順に従います。 接続の設定が完了したら、データを Customer Engagement アプリに同期する場合には、次の手順に従います。

1. LCS ページから Finance and Operations アプリを開き、ログインして、**データ管理 \> デュアル書き込み** の順に移動します。
2. データを同期するテーブルの **初期同期** 機能を実行します。

既存の Dataverse データを Finance and Operations アプリに同期するには、次の手順に従います。

1. Finance and Operations アプリに新しい会社を作成します。
2. デュアル書き込み接続の設定に会社を追加します。
3. 3 文字の ISO 会社コードを使用し、Dataverse データを [Bootstrap](bootstrap-company-data.md) にて実行します。
4. データを同期するテーブルの **初期同期** 機能を実行します。

例へのリンクや代替のアプローチについては、[使用例](#example)のセクションを参照してください。

## <a name="an-existing-finance-and-operations-app-instance-and-a-new-customer-engagement-app-instance"></a><a id="existing-new"></a>既存の Finance and Operations アプリ インスタンスと新しい Customer Engagement アプリ インスタンス

Finance and Operations アプリの既存インスタンスと Customer Engagement アプリの新規のインスタンス間のデュアル書き込み接続の設定は、Finance and Operation 環境で発生します。

1. [Finance and Operations アプリから接続を設定します](enable-dual-write.md)。
2. データを同期するテーブルの **初期同期** 機能を実行します。

例へのリンクや代替のアプローチについては、[使用例](#example)のセクションを参照してください。

## <a name="an-existing-finance-and-operations-app-instance-and-an-existing-customer-engagement-app-instance"></a><a id="existing-existing"></a>既存の Finance and Operations アプリ インスタンスと既存の Customer Engagement アプリ インスタンス

Finance and Operations アプリの既存インスタンスと Customer Engagement アプリの既存のインスタンス間のデュアル書き込み接続の設定は、Finance and Operation 環境で行います。

1. [Finance and Operations アプリから接続を設定します](enable-dual-write.md)。
2. 既存の Dataverse データを Finance and Operations アプリに同期するには、3 文字の ISO 会社コードを使用して、Dataverse データを [ブートストラップ](bootstrap-company-data.md) にて実行します。
3. データを同期するテーブルの **初期同期** 機能を実行します。

例へのリンクや代替のアプローチについては、[使用例](#example)のセクションを参照してください。

## <a name="example"></a>例

例については、[Customers V3 の有効化—連絡先テーブル マップ](enable-entity-map.md#enable-table-map)を参照してください

初期同期を実行する必要がある各エンティティのデータ ボリュームに基づく代替的なアプローチについては、[初期同期の考慮事項](initial-sync-guidance.md)を参照してください。


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]