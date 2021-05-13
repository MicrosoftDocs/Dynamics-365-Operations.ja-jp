---
title: Finance and Operations アプリの開発と管理
description: このページは、開発者と IT プロが Finance and Operations の使用を開始するのに役に立ちます。
author: robinarh
ms.date: 06/20/2017
ms.topic: index-page
ms.prod: ''
ms.technology: ''
audience: IT Pro, Developer
ms.reviewer: rhaertle
ms.custom: 62303
ms.assetid: 3d7dfc2a-4be2-4fdc-ac35-cc96868f56ab
ms.search.region: Global
ms.author: margoc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 27448c0ce06e018b4c9f40397eb2ffd1f6aea2aa
ms.sourcegitcommit: fa99a36c3d30d0c0577fd3f63ed6bf2f71599e40
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/20/2021
ms.locfileid: "5920491"
---
# <a name="development-and-administration-for-finance-and-operations-apps"></a>Finance and Operations アプリの開発と管理

[!include [banner](includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Finance and Operations アプリの開発と管理には次のものが含まれます。

- 管理者エクスペリエンスと Lifecycle Services
- 開発者エクスペリエンス
- インテリジェンス
- モバイル アプリ
- データ管理とデータ エンティティ 
- Office 統合

## <a name="developer-experience"></a>開発者エクスペリエンス
開発者エクスペリエンスは、Visual Studio と .NET コンポーネントを使用する最新のツールに基づいています。
-   開発ツールは実行中の環境から切り離されます。すなわち、オンライン データベースではなく、ローカルの XML ベース ファイル対して開発を行います。
-   Microsoft Visual Studio が開発環境です。 Finance and Operations は Visual Studio 環境をカスタマイズして、円滑で慣れ親しんだエクスペリエンスを提供します。
-   X++ コンパイラは、すべての機能に対して一般的な中間的な言語 (CIL) を生成します。 CIL は、C# プログラミング言語など、他の .NET ベース (マネージド) 言語で使用されるものと同じ中間言語です。
-   ブラウザー ベースのクライアントとフォームのデザイン パターンを活用して、改善されたエンドユーザー エクスペリエンスを提供できます。
-   Application Lifecycle Management (ALM) システムは、ビルドの自動化、テストの自動化、およびクラウドへのモデルの配置をサポートします。

詳細については、 [開発およびカスタマイズのホーム ページ](dev-tools/developer-home-page.md) を参照してください。

## <a name="administrator-experience-and-lifecycle-services"></a>管理者エクスペリエンスと Lifecycle Services
Finance、Supply Chain Management、およびコマースはクラウドでホストされます。 IT プロは、Dynamics Lifecycle Services (LCS) を使用して、環境を監視およびチューニングし、機能を配置し、最新の修正プログラムで最新の状態に維持することができます。 展開の範囲内で、セキュリティを構成し、プロセスをいつ実行するかを管理することができます。 また、ビジネス インテリジェンスとレポート、モバイル アプリ、Office、およびその他の統合のサポートを要求されたとき、LCS を使用することもできます。 

## <a name="bi--reporting"></a>BI とレポート作成
Finance and Operations は、5 つの異なるレポート エクスペリエンスを提供します。 組織全体のさまざまな職務の複雑で多様なレポートのニーズを満たすために、専門のツールが用意されています。
- 操作ビュー: 特定のビジネス ペルソナの特定のニーズに対応するように設計されています。
- ビジネス ドキュメント – 処理済みのビジネス データをキャプチャおよび交換するために使用される静的なドキュメントです。
- 分析ツールおよび視覚化 – ユーザーによるデータの検証を可能にする論理計算の個人用プレゼンテーションです。
- Electronic Reporting – 電子ドキュメントの形式の構成に使用されるツールです。
- Financial Reporting – 法人の財務活動の標準的な見解に基づいて、詳細な会計管理のツールを提供するように設計されています。

## <a name="mobile-apps"></a>モバイル アプリ
Finance and Operations のモバイル アプリは、組織の業務プロセスをモバイル化するための力を組織に与えます。 IT 管理者が組織のモバイル ワークスペース機能を有効にすると、ユーザーはアプリにサインインしてすぐにモバイル デバイスから業務プロセスの実行を開始できます。 Dynamics 365 for Finance and Operations モバイル アプリには、生産性を高めるのに役立つ次の機能が含まれています。
+ ネットワーク接続が断続的な場合やモバイル デバイスがオフラインの場合でも、ユーザーは業務データを表示、編集、および処理できます。 デバイスがネットワーク接続を再確立する際に、オフライン データ操作は Finance and Operations と自動的に同期されます。 
+ IT 管理者または開発者は、組織に合わせたモバイル ワークスペースを構築し公開することができます。 このアプリは既存のコード資産を使用します。したがって、検証手順、ビジネス ロジック、またはセキュリティのコンフィギュレーションを再実装する必要はありません。 
+ IT 管理者または開発者は、Finance and Operations Web クライアントに含まれているポイント アンド クリック ワークスペース デザイナーを使用してモバイル ワークスペースを簡単に設計できます。 
+ IT 管理者または開発者は、ビジネス ロジック拡張フレームワークを使用してワークスペースのオフライン機能を必要に応じて最適化できます。 デバイスがオフラインの間もデータは引き続き処理されるため、デバイスが常時ネットワーク接続していなくても、モバイル シナリオは豊富で流動的なままです。 

## <a name="data-management-and-data-entities"></a>データ管理とデータ エンティティ
Finance and Operations からのデータは、Dataverse、Power Apps、および Power BI を使用して、Microsoft のデータ ソースおよび Microsoft 以外のデータ ソースと簡単に統合することができます。 詳細については、 [データ エンティティの概要](data-entities/data-entities.md) を参照してください。

## <a name="office-integration"></a>Office 統合
Microsoft Office の統合機能は、生産的環境を提供し、Office 製品を使用して作業を遂行するユーザーを支援します。 詳細については、 [Office 統合の概要](office-integration/office-integration.md) を参照してください。

## <a name="elearning-courses"></a>eLearning コース
オンライン コースおよびトレーニングについては、[Microsoft Learn の Dynamics 365 Finance and Operations ](/learn/browse/?expanded=dynamics-365&products=dynamics-finance-operations&roles=administrator%2cdeveloper) をご確認ください。


[!INCLUDE[footer-include](../../includes/footer-banner.md)]