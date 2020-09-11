---
title: デュアル書き込み設定用にサポートされたシナリオ
description: このトピックでは、デュアル書き込みの設定でサポートされているシナリオについて説明します。
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 08/17/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-01-06
ms.openlocfilehash: 275d24d8f32fd1d2d15356d14c5c6591e8503c65
ms.sourcegitcommit: ec4df354602c20f48f8581bfe5be0c04c66d2927
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/19/2020
ms.locfileid: "3706255"
---
# <a name="supported-scenarios-for-dual-write-setup"></a>デュアル書き込み設定用にサポートされたシナリオ

[!include [banner](../../includes/banner.md)]

[!include [preview-banner](../../includes/preview-banner.md)]

Finance and Operations 環境と Common Data Service 環境との間には、デュアル書き込み接続を設定できます。

+ **Finance and Operations 環境** では、**Finance and Operations アプリ** の基盤となるプラットフォームを提供します (たとえば、Microsoft Dynamics 365 Finance、Dynamics 365 Supply Chain Management、Dynamics 365 Retail)。
+ **Common Data Service 環境**では、**Dynamics 365 のモデル駆動型アプリ**の基盤となるプラットフォームを提供します (Dynamics 365 Sales、Dynamics 365 Customer Service、Dynamics 365 Field Service、Dynamics 365 Marketing、および Dynamics 365 Project Service Automation)。

>[!IMPORTANT]
>Finance and Operations の Human Resources では 、デュアル書き込み接続をサポートしていますが、Dynamics 365 Human Resources アプリではサポートされていません。

この設定のメカニズムは、サブスクリプションおよび環境によって異なります。

+ Finance and Operations アプリの新しいインスタンスの場合、デュアル書き込み接続の設定は Microsoft Dynamics Lifecycle Services (LCS) で開始されます。 Microsoft Power Platform のライセンスを所有している際は、テナントに無い場合、新しい Common Data Service 環境が得られます。
+ 既存のインスタンス Finance and Operations アプリの場合、デュアル書き込み接続の設定は Finance and Operations環境で開始されます。

サポートされている設定シナリオは次のとおりです。

+ [新しい Finance and Operations アプリ インスタンスと新しいモデル駆動型アプリ インスタンス](#new-new)
+ [新しい Finance and Operations アプリ インスタンスと既存のモデル駆動型アプリ インスタンス](#new-existing)
+ [デモ データ付き新しい Finance and Operations アプリ インスタンスと新しいモデル駆動型アプリ インスタンス](#new-demo-new)
+ [デモ データ付き新しい Finance and Operations アプリ インスタンスと既存のモデル駆動型アプリ インスタンス](#new-demo-existing)
+ [既存の Finance and Operations アプリ インスタンスと新規または既存のモデル駆動型アプリ インスタンス](#existing-existing)

## <a name="a-new-finance-and-operations-app-instance-and-a-new-model-driven-app-instance"></a><a id="new-new"></a>新しい Finance and Operations アプリ インスタンスと新しいモデル駆動型アプリ インスタンス

データ無しの Finance and Operations アプリの新しいインスタンスと Dynamics 365 のモデル駆動アプリの新しいインスタンス間のデュアル書き込み接続を設定するには、[Lifecycle Services からのデュアル書き込み設定](lcs-setup.md) の手順に従います。 接続の設定が完了すると、次のアクションが自動的に実行されます。

- 新しい空の Finance and Operations 環境が準備されます。
- モデル駆動型のアプリの新しい空のインスタンスがプロビジョニングされ、CRM の主要ソリューションがインストールされます。
- DAT 会社のデータに対して、デュアル書き込み接続が確立されます。
- エンティティ マップでは、ライブ同期が有効になっています。

次に、両方の環境について、ライブ データ同期の準備が整います。

## <a name="a-new-finance-and-operations-app-instance-and-an-existing-model-driven-app-instance"></a><a id="new-existing"></a> 新しい Finance and Operations アプリ インスタンスと既存のモデル駆動型アプリ インスタンス

データ無しの Finance and Operations アプリの新しいインスタンスと Dynamics 365 のモデル駆動アプリの既存インスタンス間のデュアル書き込み接続を設定するには、[Lifecycle Services からのデュアル書き込み設定](lcs-setup.md) の手順に従います。 接続の設定が完了すると、次のアクションが自動的に実行されます。

- 新しい空の Finance and Operations 環境が準備されます。
- DAT 会社のデータに対して、デュアル書き込み接続が確立されます。
- エンティティ マップでは、ライブ同期が有効になっています。

次に、両方の環境について、ライブ データ同期の準備が整います。

既存の Common Data Service データを Finance and Operations アプリに同期するには、次の手順に従います。

1. Finance and Operations アプリに新しい会社を作成します。
2. デュアル書き込み接続の設定に会社を追加します。
3. 3 文字の国際標準化機構 (ISO) 会社コードを使用し、Common Data Service データを [Bootstrap](bootstrap-company-data.md) にて実行します。

デュアル書き込みはライブ同期モードになっているため、Common Data Service からのデータは、自動的に Finance and Operations アプリに送られます。

## <a name="a-new-finance-and-operations-app-instance-that-has-demo-data-and-a-new-model-driven-app-instance"></a><a id="new-demo-new"></a> デモ データ付きの新しい Finance and Operations アプリ インスタンスと新しいモデル駆動型アプリ インスタンス

デモ データ付き Finance and Operations アプリの新しいインスタンスと Dynamics 365 モデル駆動型アプリの新しいインスタンス間にデュアル書き込み接続を設定するには、このトピック前半の[新しい Finance and Operations アプリ インスタンスと新しいモデル駆動型アプリ インスタンス](#new-new) セクションにある手順に従います。 接続の設定が完了したら、デモ データをモデル駆動型のアプリに同期する場合には、次の手順に従います。

1. LCS ページから Finance and Operations アプリを開き、ログインして、**データ管理 \> デュアル書き込み**の順に移動します。
2. データを同期するエンティティの**初期同期**機能を実行します。

## <a name="a-new-finance-and-operations-app-instance-that-has-demo-data-and-an-existing-model-driven-app-instance"></a><a id="new-demo-existing"></a> デモ データ付きの新しい Finance and Operations アプリ インスタンスと既存のモデル駆動型アプリ インスタンス

デモ データ付き Finance and Operations アプリの新しいインスタンスと Dynamics 365 モデル駆動型アプリの既存インスタンス間にデュアル書き込み接続を設定するには、このトピック前半の[新しい Finance and Operations アプリ インスタンスと既存モデル駆動型アプリ インスタンス](#new-existing) セクションにある手順に従います。 接続の設定が完了したら、デモ データをモデル駆動型のアプリに同期する場合には、次の手順に従います。

1. LCS ページから Finance and Operations アプリを開き、ログインして、**データ管理 \> デュアル書き込み**の順に移動します。
2. データを同期するエンティティの**初期同期**機能を実行します。

既存の Common Data Service データを Finance and Operations アプリに同期するには、次の手順に従います。

1. Finance and Operations アプリに新しい会社を作成します。
2. デュアル書き込み接続の設定に会社を追加します。
3. 3 文字の ISO 会社コードを使用し、Common Data Service データを [Bootstrap](bootstrap-company-data.md) にて実行します。

デュアル書き込みはライブ同期モードになっているため、Common Data Service からのデータは、自動的に Finance and Operations アプリに送られます。

## <a name="an-existing-finance-and-operations-app-instance-and-a-new-or-existing-model-driven-app-instance"></a><a id="existing-existing"></a> 既存の Finance and Operations アプリ インスタンスと新規または既存のモデル駆動型アプリ インスタンス

Finance and Operations アプリの既存インスタンスと Dynamics 365 のモデル駆動型アプリの新規または既存インスタンス間のデュアル書き込み接続の設定は、Finance and Operation 環境で発生します。

1. Finance and Operations アプリから接続を設定します。
2. 既存の Common Data Service データを Finance and Operations アプリに同期するには、3 文字の ISO 会社コードを使用して、Common Data Service データを [ブートストラップ](bootstrap-company-data.md) にて実行します。

デュアル書き込みはライブ同期モードになっているため、Common Data Service からのデータは、自動的に Finance and Operations アプリに送られます。
