---
title: 二重書き込みの概要
description: このトピックでは、二重書き込みの概要について説明します。 二重書き込みは、Microsoft Dynamics 365 モデル駆動型のアプリと Finance and Operations アプリの間の、ほぼリアルタイムの対話を提供するインフラストラクチャです。
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 02/06/2020
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
ms.openlocfilehash: 64626ebdd7fbad3d47a4b4c6bbc45bf3bc0c8277
ms.sourcegitcommit: 68f1485de7d64a6c9eba1088af63bd07992d972d
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/27/2020
ms.locfileid: "3172787"
---
# <a name="dual-write-overview"></a>二重書き込みの概要

[!include [banner](../../includes/banner.md)]



## <a name="what-is-dual-write"></a>二重書き込みとは何ですか?

二重書き込みは、Microsoft Dynamics 365 モデル駆動型のアプリと Finance and Operations アプリの間の、ほぼリアルタイムの対話を提供する標準のインフラストラクチャです。 顧客、製品、人材、および業務に関するデータがアプリケーション境界を超えてフローする場合、組織のすべての部門が権利を持つことになります。

二重書き込みは、Finance and Operations アプリと Common Data Service の間で密に結合された双方向の統合を提供します。 Finance and Operations アプリでのデータの変更によって Common Data Service 書き込みが行われ、Common Data Service のデータの変更によって Finance and Operations アプリケーションへの書き込みが行われます。 この自動化されたデータ フローによって、アプリ間で統合されたユーザー エクスペリエンスが提供されます。

![アプリ間のデータの関係](media/dual-write-overview.jpg)

二重書き込みには、*インフラストラクチャ*の側面と*アプリケーション*の側面の 2 つの側面があります。

### <a name="infrastructure"></a>インフラストラクチャ

二重書き込みインフラストラクチャは、拡張性と信頼性を備えており、次の主な機能を備えています。

+ アプリケーション間の同期および双方向のデータ フロー
+ 同期と、オンラインおよびオフライン/非同期モードでシステムをサポートするための再生、一時停止、キャッチ アップの各モードとの組み合わせ。
+ アプリケーション間で初期データを同期する機能
+ データ管理者の活動とエラー ログの統合ビュー
+ カスタム警告としきい値をコンフィギュレーションし、通知をサブスクライブする機能
+ フィルタリングと変換のための直観的なユーザー インターフェイス (UI)
+ エンティティの相互関係と関係を設定および表示する機能
+ 標準エンティティとカスタム エンティティおよびマップの両方に対する拡張性
+ 信頼できるアプリケーション ライフサイクル管理
+ 新しい顧客に対する標準の設定エクスペリエンス

### <a name="application"></a>申請

二重書き込みでは、Finance and Operations アプリと Dynamics 365 のモデル駆動型アプリにおける概念の間にマッピングが作成されます。 この統合により、次のシナリオがサポートされます。

+ 統合された顧客マスター
+ 顧客ロイヤルティ カードおよび報酬ポイントへのアクセス
+ 統一された製品マスタリング エクスペリエンス
+ 組織階層の認識
+ 統合された仕入先マスター
+ 財務および税参照データへのアクセス
+ オンデマンドの価格エンジンのエクスペリエンス
+ 統合された見込み顧客エクスペリエンス
+ フィールド エージェントを介して社内資産と顧客資産の両方を提供する機能
+ 統合された仕入れから支払エクスペリエンス
+ 顧客データおよびドキュメントに関する統合された活動とメモ
+ 手持在庫状態および詳細を検索する機能
+ プロジェクトの現金化エクスペリエンス
+ 関係者の概念を使用して複数の住所と役割を処理する機能
+ ユーザーに対する単一のソース管理
+ 小売業とマーケティング向けの統合チャネル
+ プロモーションと割引の可視性
+ サービス要求機能
+ 合理化されたサービス工程

## <a name="top-reasons-to-use-dual-write"></a>二重書き込みを使用する主な理由

二重書き込みにより、Microsoft Dynamics 365 アプリケーション間でデータの統合が提供されます。 この信頼性の高いフレームワークでは、環境をリンクして、さまざまなビジネス アプリケーションを連携させることができます。 二重書き込みを使用する必要がある主な理由は次のとおりです。

+ 二重書き込みは、Finance and Operations アプリと Dynamics 365 の モデル駆動型アプリの間で密結合、ほぼリアルタイム、および双方向の統合を提供します。 この統合により、すべてのビジネスソリューションに対して、1 つの停止ショップとして Microsoft Dynamics 365 が作成されます。 Dynamics 365 Finance と Dynamics 365 Supply Chain Management を使用しているが、顧客関係管理 (CRM) に対して Microsoft 以外のソリューションを使用している顧客は、二重書き込みをサポートするために Dynamics 365 に移行しています。
+ 顧客、製品、工程、プロジェクト、およびインターネット オブ シングス (IoT) のデータは、自動的に二重書き込みによって Common Data Service にフローします。 この接続は、Microsoft Power Platform の展開に関心のある企業にとって非常に便利です。
+ 二重書き込みインフラストラクチャは、コードなし/ロー コード原則に従います。 標準のテーブルからテーブルへのマップを拡張したり、カスタム マップを含めたりするには、最小限のエンジニアリング実績が要求されます。
+ 二重書き込みでは、オンライン モードとオフライン モードの両方がサポートされます。 Microsoft は、オンラインとオフライン モードのサポートを提供している唯一の会社です。

## <a name="what-does-dual-write-mean-for-users-and-architects-of-crm-products"></a>CRM 製品のユーザーと設計者における二重書き込みの意味は何ですか?

二重書き込みでは、Finance and Operations アプリと Common Data Service 間のデータ フローを自動化します。 将来のリリースでは、Dynamics 365 のモデル駆動アプリ (顧客、連絡先、見積、注文など) の概念が、中規模市場および本社の顧客に縮小増幅されます。

最初のリリースでは、自動化のほとんどは二重書き込みソリューションによって処理されます。 今後のリリースでは、これらのソリューションは Common Data Service に含まれるようになります。 Common Data Service への今後の変更点を理解することにより、長期的に実績を節約することができます。 次に重要変更のいくつかを挙げます。

+ Common Data Service に会社や関係者などの新しい概念が追加されます。 これらの概念は、Dynamics 365 Sales、Dynamics 365 Marketing、Dynamics 365 Customer Service、および Dynamics 365 Field Service など、Common Data Service に構築されているすべてのアプリに影響します。
+ 活動とメモは統合されており、C1s (システムのユーザー) と C2s (システムの顧客) の両方をサポートするように拡張されています。
+ 次に Common Data Service の変更のいくつかを挙げます。

    - 10 進データ型によって金額データ型が置き換えられます。
    - 日付の有効期間は、過去、現在、将来のデータを同じ場所にサポートします。
    - 通貨と為替レートはより詳細にサポートされ、**為替レート**のアプリケーション プログラミング インターフェイス (API) が更新されます。
    - 単位換算がサポートされます。

今後の変更の詳細については、[Data in Common Data Service – phase 1 & 2](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/finance-operations-crossapp-capabilities/data-common-data-service-phase-1) を参照してください。
