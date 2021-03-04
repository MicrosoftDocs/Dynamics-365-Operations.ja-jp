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
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-01-06
ms.openlocfilehash: 85530cf644c7b7ffe922a6fb3288f4e05c5df91c
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 12/05/2020
ms.locfileid: "4685616"
---
# <a name="dual-write-overview"></a>二重書き込みの概要

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]



## <a name="what-is-dual-write"></a>二重書き込みとは何ですか?

二重書き込みは、Customer Engagement アプリと Finance and Operations アプリの間の、ほぼリアルタイムの対話を提供する標準のインフラストラクチャです。 顧客、製品、人材、および業務に関するデータがアプリケーション境界を超えてフローする場合、組織のすべての部門が権利を持つことになります。

二重書き込みは、Finance and Operations アプリと Dataverse の間で密に結合された双方向の統合を提供します。 Finance and Operations アプリでのデータの変更によって Dataverse 書き込みが行われ、Dataverse のデータの変更によって Finance and Operations アプリケーションへの書き込みが行われます。 この自動化されたデータ フローによって、アプリ間で統合されたユーザー エクスペリエンスが提供されます。

![アプリ間のデータの関係](media/dual-write-overview.jpg)

二重書き込みには、*インフラストラクチャ* の側面と *アプリケーション* の側面の 2 つの側面があります。

### <a name="infrastructure"></a>インフラストラクチャ

二重書き込みインフラストラクチャは、拡張性と信頼性を備えており、次の主な機能を備えています。

+ アプリケーション間の同期および双方向のデータ フロー
+ 同期と、オンラインおよびオフライン/非同期モードでシステムをサポートするための再生、一時停止、キャッチ アップの各モードとの組み合わせ。
+ アプリケーション間で初期データを同期する機能
+ データ管理者の活動とエラー ログの結合ビュー
+ カスタム警告としきい値をコンフィギュレーションし、通知をサブスクライブする機能
+ フィルタリングと変換のための直観的なユーザー インターフェイス (UI)
+ エンティティの相互関係と関係を設定および表示する機能
+ 標準テーブルとカスタム テーブルおよびマップの両方に対する拡張性
+ 信頼できるアプリケーション ライフサイクル管理
+ 新しい顧客に対する標準の設定エクスペリエンス

### <a name="application"></a>申請

二重書き込みでは、Finance and Operations アプリと Customer Engagement アプリにおける概念の間にマッピングが作成されます。 この統合により、次のシナリオがサポートされます。

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
+ 顧客、製品、工程、プロジェクト、およびインターネット オブ シングス (IoT) のデータは、自動的に二重書き込みによって Dataverse にフローします。 この接続は、Power Platform の展開に関心のある企業にとって便利です。
+ 二重書き込みインフラストラクチャは、コードなし/ロー コード原則に従います。 標準のテーブルからテーブルへのマップを拡張したり、カスタム マップを含めたりするには、最小限のエンジニアリング実績が要求されます。
+ 二重書き込みでは、オンライン モードとオフライン モードの両方がサポートされます。 Microsoft は、オンラインとオフライン モードのサポートを提供している唯一の会社です。

## <a name="what-does-dual-write-mean-for-developers-and-architects-of-customer-engagement-apps"></a><a id="developer-architect"></a>二重書き込みは、Customer Engagement アプリの開発者と設計者にとって何を意味しますか?

二重書き込みは、Finance and Operations アプリと Customer Engagement アプリ間のデータ フローを自動化します。 二重書き込みは、Dataverse にインストールされている 2 つの AppSource ソリューションで構成されています。 ソリューションは、Dataverse のエンティティ スキーマ、プラグイン、ワークフローを展開して、ERP サイズに合わせて拡張できるようにします。 実装を成功させるためには、Customer Engagement アプリの開発者や設計者は、これらの変更点を理解し、Finance and Operations アプリ上で担当者と協力する必要があります。

Finance and Operations アプリケーションと同等の機能を作成するために、二重書き込みは Dataverse スキーマにいくつかの重要な変更を加えます。 計画を理解すれば、将来の設計や開発のやり直しを回避できます。

+ 二重書き込み AppSource パッケージがインストールされると、Dataverse は会社や関係者などの新しい概念を持つようになります。 これらの概念は、Dynamics 365 Sales、Dynamics 365 Marketing、Dynamics 365 Customer Service、Dynamics 365 Field Service を含む、Dataverse 上に構築されたアプリケーションが、Finance and Operations アプリとシームレスとやりとりするのに役立ちます。

+ 活動とメモは統合されており、C1s (システムのユーザー) と C2s (システムの顧客) の両方をサポートするように拡張されています。

+ Finance and Operations アプリと Dataverse 間の通貨転送中のデータ損失を防ぐために、Customer Engagement アプリの通貨のデータ型で小数点以下の桁数を拡張することができます。 この機能は、既存の行をメタデータ レイヤーで新しい拡張状態に自動変換します。 このプロセス中に、通貨の値は、money データではなく10進数データに変換され、通貨の値は小数点以下 10 桁をサポートします。 この機能はオプトインであり、小数点以下 4 桁を超える精度を必要としない組織はオプトインする必要はありません。 詳細については、[二重書き込みの通貨データ型の移行](currrency-decimal-places.md) を参照してください。

+ [日付の有効期間](../../dev-tools/date-effectivity.md) は Dataverse に追加されます。 同じエンティティ上の過去、現在、将来のデータをサポートします。

+ 製品の [単位換算](../../../../supply-chain/pim/tasks/manage-unit-measure.md) では、製品、見積、注文、および請求書がサポートされています。

今後の変更の詳細については、[二重書き込みの新機能および変更された機能](whats-new-dual-write.md) を参照してください。



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]