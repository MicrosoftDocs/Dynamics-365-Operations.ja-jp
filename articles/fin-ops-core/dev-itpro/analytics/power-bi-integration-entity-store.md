---
title: エンティティ格納と Power BI の統合
description: この記事では、エンティティ格納が Power BI 統合を有効にする方法について説明します。
author: MilindaV2
ms.date: 06/16/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: IT Pro
ms.reviewer: sericks
ms.search.region: Global
ms.author: milindav
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: Platform update 1
ms.custom: 265974
ms.assetid: 434b5d9f-9877-4769-ad96-d4e8d460a7fa
ms.search.form: BIMeasurementDeployManagementEntityStore
ms.openlocfilehash: abe7b0b85103f202aa1c890fb5b44e7bbb4c7ada
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/12/2022
ms.locfileid: "9273044"
---
# <a name="power-bi-integration-with-entity-store"></a>エンティティ格納と Power BI の統合

[!include [banner](../includes/banner.md)]

エンティティ格納は、Microsoft Dynamics 365 Finance に含まれている運用データ ストアです。 この記事では、エンティティ格納が Power BI 統合を有効にする方法について説明します。

エンティティ格納は、アプリケーションに含まれている運用データ ストアです。 エンティティ格納の機能は、Microsoft Dynamics AX プラットフォーム更新プログラム 1 (2016 年 5 月) リリースで導入されました。 この機能を使用すると、管理者またはパワーユーザーは、レポートおよび分析用の専用データストアで測定値を公開できます。 (集計の測定は、エンティティを使用してモデル化されたスター スキーマです)。このデータ ストアをエンティティ格納と呼びます。 レポート用に最適化されたデータベースです。 エンティティ格納では、Microsoft SQL Server に組み込まれたメモリ内の集合縦棒ストア インデックス (CCI) 機能を使用して、レポートとクエリを最適化します。 顧客は、Microsoft Power BI の DirectQuery モデルをエンティティ格納と共に使用し、大量のデータに対して大量のほぼリアルタイムの分析レポートを有効にすることができます。

## <a name="power-bi-directquery-mode"></a>Power BI DirectQuery モード
Microsoft Dynamics AX の 2016 年 2 月のリリースでは、データ エンティティ (集計データのエンティティと、詳細または通常のデータ エンティティの両方) で公開される OData エンドポイントを使用して Power BI レポートを作成することができました。 この方法は引き続き サポートされていますが、エンティティ格納でもパワー ユーザーは Power BI DirectQuery レポートを作成できます。

[![DirectQuery モード。](./media/entity-store-architecture-1024x587.jpg)](./media/entity-store-architecture.jpg)

前の図に示すように、DirectQuery はエンティティ格納で直接レポートを実行するレポート モードです。 このレポート モードでは、データは Power BI のキャッシュにステージングされません。 このモードでは、2 つの直接的な利点があります。

- 大量のデータに対して Power BI レポートを作成することができます。
- レポートは、Power BI を使って更新する必要がなくなります。 エンティティ格納が更新されると、レポートに最新のデータが反映されます。

さらに、Power BI サービスにデータがキャッシュされないため、データが環境から離れることはありません。

## <a name="stage-aggregate-measurements-in-entity-store"></a>エンティティ格納における集計測定のステージング
集計測定は分析シナリオのためにモデル化されたスター スキーマです。 2016 年 2 月のリリースでは、リアルタイムなメモリ内集計の測定が有効になりました。 リアルタイムの集計測定を使用することにより、データのリアルタイム操作に対応する埋め込みチャートおよび主要業績評価指標 (KPI) を有効にすることができます。 詳細については、 [Analysis Services キューブから集計モデルへの移行](../migration-upgrade/in-memory-real-time-aggregate-models.md) を参照してください。 リアルタイム集計測定は、インメモリの非クラスター化縦棒ストア インデックス (NCCI) の技術を活用します。 リアルタイムの集計の測定で作成されたビジュアルおよび集計計算に数秒以内のトランザクションが反映されます。 プラットフォーム更新プログラム 1 (2016 年 5 月) のリリースでは、エンティティ格納でステージングできる集計測定を有効にしました。 エンティティ ストアで実施された集計測定は、Power BI を使用して大量のデータを調べる必要がある、ほぼリアルタイムの分析シナリオで使用できます。 開発者として、 [集計データのモデリング](model-aggregate-data.md) でリアルタイム分析の集計測定をモデル化する方法について確認することができます。 プラットフォーム更新プログラム 1 (2016 年 5 月) のリリースでは、エンティティ格納でステージングできる集計測定をモデル化する機能も追加しました。 Microsoft Visual Studio で、**StagedEntityStore** を集計の測定の用途プロパティとして指定します。 この新しいプロパティは、2016 年 5 月で追加されました。 以前は、**InMemoryRealTime** は用途プロパティとして使用できました。

![Visual Studio にある新しい StagedEntityStore の使用プロパティ。](media/new-usage-property-in-VS.png)

ただし、ステージングできるように集計測定をモデル化するのはなぜかと疑問に思われるかもしれません。 メモリ内リアルタイム集計測定を常に使用しないのはなぜですか。 **StagedEntityStore** パターンを使用する理由はいくつかあります。

- 調査して分析する必要がある、大量のデータが存在する可能性があります。
- コード アップグレード プロセスの一部として、Microsoft Dynamics AX 2012 R3 から移行した解析プロジェクト (つまり、キューブ) がある場合があります。 スキーマには複雑なビューと結合が存在するため、クエリ応答時間は埋め込まれたビジュアルには受け入れられない場合があります。 ただし、NCCI テクノロジーを直ちに活用するためにビジュアルをリファクタリングする必要はありません。
- 運用データベースのスキーマとは異なり、エンティティ ストアのスキーマは特にレポートのためにモデル化されています。 したがって、エンティティ ストアのスキーマから新しいレポートを作成する方がはるかに簡単です。
- 自分のシナリオが、操作の数秒以内での分析データの更新を必要としない場合があります。 データ検索を有効にするために構築されているほとんどの Power BI レポートは、このカテゴリに分類されます。 約 10 分でデータをリフレッシュすることがシナリオで許容される場合は、段階的なパターンを使用する場合があります。

上記の理由のいずれかによってユーザーの状況がカバーされる場合、エンティティ店舗で集計測定を実行し、Power BI 統合に対して使用する必要があります。

## <a name="update-entity-store"></a>エンティティ店舗の更新
エンティティ格納が自動化され、システムにより管理されます。 クライアントで、**エンティティ格納** ページは **システム管理** &gt; **設定** &gt; **エンティティ格納** で表示できます。 詳細については、[エンティティ格納の自動化更新](./automated-entity-store-refresh.md)を参照してください。

### <a name="connecting-to-the-entity-store-database"></a>エンティティ格納データベースに接続する
トラブルシューティングや診断の場合、関連するサンドボックス環境から直接エンティティ格納データベースに接続することができます。  接続するには

1. サンドボックスにアクセスするには、リモート デスクトップを使用します。  RDP ファイルは、IP アドレスをセーフ リストに登録後、**環境の詳細** ページからダウンロードできます。
2. SQL Server Management Studio を開き、**環境の詳細** ページで指定したサーバーに接続します。  
    * **データベース アカウント** というセクションを見つけます。  名前 **axdwadmin** を持つユーザーのエントリを探します。  
    * サーバー名は、**SQL サーバー\データベース名** フィールドの最初の部分です。  これは、**SQLServerName.database.windows.net** の形式で使用する必要があります。ここで、SQLServerName は LCS からの値です。
    * 認証の種類は、Windows 認証から SQL Server 認証に変更する必要があります。
    * ログインは、axdwadmin となり、パスワードは LCS からの値となります。
3. **オプション** ボタンを使用するか **接続のプロパティ** タブを参照して、**データベースに接続** プロパティを既定値から、LCS からの **データベース名** 値に変更します。
4. **接続** をクリックしてデータベースにアクセスします。


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
