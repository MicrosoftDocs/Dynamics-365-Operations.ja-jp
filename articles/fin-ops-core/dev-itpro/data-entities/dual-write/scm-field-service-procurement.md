---
title: Supply Chain Management と Field Service の間の調達の統合
description: このトピックでは、デュアル書き込み統合で Supply Chain Management と Field Service の両方からの発注書の作成と更新をサポートする方法について説明します。
author: RamaKrishnamoorthy
ms.date: 11/11/2020
ms.topic: article
audience: Application User
ms.reviewer: tfehr
ms.search.region: Global
ms.author: tfehr
ms.search.validFrom: 2020-11-11
ms.dyn365.ops.version: Release 10.0.17
ms.openlocfilehash: ab251ee60bf3c831b0139beb9557c6b3faaf9f66
ms.sourcegitcommit: 9acfb9ddba9582751f53501b82a7e9e60702a613
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/10/2021
ms.locfileid: "7783286"
---
# <a name="integrate-procurement-between-supply-chain-management-and-field-service"></a>Supply Chain Management と Field Service の間の調達の統合

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

Microsoft Dynamics 365 Supply Chain Management は、信頼性の高い調達機能を提供します。 Dynamics 365 Field Service には、サービス プロセスに関連付けられた購買プロセスをサポートするのと同様の機能が用意されています。 この 2 つのアプリケーションの機能は、デュアル 書き込みによって統合され、テーブル マッピング、ソリューション ロジック、ビュー、フォームを通じて、機能間の利用ケースを実現できます。

この統合により、発注書の作成と、ほとんどの場合、両方のアプリケーションからの更新がサポートされます。 ただし、Supply Chain Management では価格決定、住所、製品受領が制御されます。 Field Service と Supply Chain Management の両方を使用する組織では、機能間の強力なユース ケースがいくつか有効になります。 これらのユース ケースによって、調達が開始され、両方のシステムにわたって追跡されます。

次の図は、両方のシステムのテーブルと、テーブルが互いにマップされている方法を示しています。 Field Service の発注書は *アカウント* の行を参照し、Supply Chain Management の発注書は *仕入先*  行を参照します。 統合を解決するために、デュアル書き込みでは、参照を使用して *仕入先* 行を *アカウント* 行とリンクします。 詳細については、[統合された仕入先マスター](vendor-mapping.md) を参照してください。

![調達のマッピング。](media/scm-field-service-tables.png)

## <a name="prerequisites"></a>必要条件

 Supply Chain Management を Field Service と統合するには、次のコンポーネントをインストールする必要があります。

- Field Service のバージョン 8.8.31.60 以降、包括的な発注書統合用
- Supply Chain Management バージョン 10.0.14 以降
- デュアル書き込みで、One GIFSCM ソリューションを実行する場合

## <a name="installation-guidelines"></a>インストール ガイドライン

### <a name="prerequisites"></a>必要条件

- **デュアル書き込み** – 詳細については、[デュアル書き込みホームページ](dual-write-home-page.md#dual-write-setup) をご覧ください。
- **Dynamics 365 Field Service** – 詳細については、[Dynamics 365 Field Service のインストール方法](/dynamics365/field-service/install-field-service#step-1-install-dynamics-365-field-service) をご覧ください。

この機能が  Microsoft Dataverse で有効な場合は、デュアル書き込みおよび Field Service により、新しいメタデータ、フォーム、ビュー、ロジックで環境を拡張する複数のソリューション レイヤーが導入されます。 これらのソリューションは、任意の順序で有効にできます。通常、次の順序でインストールします。

1. **Field Service Common** - Field Service Common が環境にインストールされている場合は、Field Service Common がインストールされています。
2. **Field Service (Anchor)** - Field Service (Anchor) が環境にインストールされている場合は、Field Service がインストールされています。 
3. **Supply Chain Management Extended** - 環境でデュアル 書き込みを有効にすると、Supply Chain Management Extended が自動的にインストールされます。 
4. **One GIFSCM ソリューション** - One GIFSCM は、どちらかのソリューション (Field Service または Supply Chain Management) が最後にインストールするソリューション によって自動的にインストールされます。

    - Field Service が既に環境にインストールされている場合に、Supply Chain Management Extended をインストールするデュアル書き込みを有効にした場合は、OneFSSCM がインストールされます。
    - Supply Chain Management Extended が既に環境にインストールされている場合に、Field Service をインストールする場合は、OneFSSCM がインストールされます。

## <a name="initial-synchronization"></a>初期同期

新しい発注書を作成して既存の発注書を処理するには、Supply Chain Management と Dataverse との間の参照データを同期する必要があります。 最初の書き込み機能を使用して、テーブルの関係を検出し、特定のマップで有効にする必要があるテーブルを探します。

次のテーブルを同期する必要があります。

- 製品テンプレート

    最初の書き込みを実行すると、必要なテーブルの完全な一覧が表示されます。 これらのテンプレートの例を次に示します。

    - すべての製品
    - リリース済製品 V2
    - Dataverse リリース済特徴的製品

- サイト
- 倉庫
- 調達カテゴリのテンプレート

    これらのテンプレートの例を次に示します。

    - 調達カテゴリ
    - プロ
    - 製品カテゴリ階層
    - 製品カテゴリの割り当て

- 仕入先テンプレート (仕入先 V2 など)
- 連絡担当者テンプレート (Dataverse 連絡先 V2 など)
- 作業者テンプレート (作業者など)

テーブルを同期することで、Supply Chain Management のすべてのドキュメント (発注書および製品受領) が Dataverse で確実に使用できます。

### <a name="account-and-vendor-tables"></a>アカウントと仕入先テーブル

Field Service での発注書は、仕入先を追跡するアカウント テーブルに依存します。 したがって、発注書の Dataverse テーブルでは、仕入先を追跡するアカウントを使用します。 この重要な違いに対応するには、アカウントと仕入先を同期するために次の 4 つのワークフローを有効にする必要があります。 

- アカウント テーブルでの仕入先の作成
- 仕入先テーブルでの仕入先の作成
- アカウント テーブルでの仕入先の更新
- 仕入先テーブルでの仕入先の更新

One GIFSCM がインストールされている場合は、Field Service and Supply Chain Management Extended の両方がインストールされているから、これらのワークフローは自動的に有効化されます。 Field Service にインストールされていないが、発注書テーブルが Dataverse と統合されていない場合は、これらのワークフローを有効化する必要があります。 どちらの場合も、最初から始めない限り、発注書を作成する前に、すべての仕入先を Dataverse でアカウントとして作成する必要があります。 それ以外の場合は、エラーが発生する場合があります。

### <a name="initial-synchronization"></a>初期同期

すべての前提条件が満たされた後に、既存の発注書と製品受領を両方のシステムで使用可能にするには、次のテンプレートの初期同期を実行する必要があります。

- 発注書ヘッダー V2
- CDS 発注書明細行
- CDS 発注書明細行のソフト削除
- 発注書の受領
- 発注書受領製品

## <a name="mappings-with-logic"></a>ロジックを使用したマッピング

この調達統合では、次のロジックに従って製品マッピングが拡張され、以下の製品テーブルで **Field Service 製品タイプ** 列が Dataverse で正しく設定されます。

- **製品タイプ** が *製品* に設定され、**品目モデル グループ、在庫製品** が *真* に設定されている場合、**Field Service 製品タイプ** は *在庫* に設定されます。
- **製品タイプ** が *製品* に設定され、**品目モデル グループ、在庫製品** が *偽* に設定されている場合、**Field Service 製品タイプ** は *非在庫* に設定されます。
- **製品タイプ** が *サービス* に設定されている場合、**Field Service 製品タイプ** が *サービス* に設定されます。

さらに、Dataverse には自分たちにに関連するアカウントを仕入先にマップするロジックも含まれます。 このロジックは、既定の請求仕入先アカウントを設定します。 作成時に、サーバー側のプラグイン ロジックにより、そのアカウントに関連付されている仕入先からの既定の請求仕入先が設定されます。 この仕入先には、この値の設定に使用される請求アカウントへの参照があります。

## <a name="supported-scenarios"></a>サポートされているシナリオ

- 発注書は、Dataverse ユーザーが作成および更新できます。 ただし、このプロセスとデータは Supply Chain Management で制御されます。 Supply Chain Management の発注書列の更新に対する制約は、Field Service からの更新の場合に適用されます。 たとえば、発注書が確定した場合は更新できない場合があります。 
- Supply Chain Management で発注書が変更管理によって制御される場合、Field Service ユーザーは、Supply Chain Management の承認ステータスが *ドラフト* の場合にのみ発注書を更新 できます。
- いくつかの列は Supply Chain Management でのみ管理され、Field Service で更新できません。 更新できない列については、製品のマッピング テーブルを確認してください。 便宜上、多くの列では、Dataverse ページ上で読み取り専用に設定されています。 

    たとえば、価格情報の列は Supply Chain Management によって管理されます。 Supply Chain Management には、Field Service の特典を提供する取引契約があります。 **単価**、**割引**、**正味金額** などの列は、Supply Chain Management からのみ表示されます。 価格が Field Service と同期を行う場合は、発注書データを入力するときに、Dataverse で **発注書** ページと **発注書製品** ページの **同期** 機能を使用する必要があります。 詳細については、[オンデマンドの Dynamics 365 Supply Chain Management 調達データでの同期](#sync-procurement) を参照してください。

- Supply Chain Management には発注書の最新の合計はないので、**合計** 列は Field Service でのみ使用できます。 Supply Chain Management の合計は、Field Service で使用できない複数のパラメータに基づいて計算されます。
- 調達カテゴリだけが指定されている発注書明細行、または指定された製品が *サービス* 製品タイプまたは Field Service 製品タイプの品目である場合は、Supply Chain Management でのみ開始できます。 明細行が同期され、Field Service で Dataverse に表示されます。
- Supply Chain Management ではなく Field Service だけがインストールされている場合、発注書では **倉庫** 列は必須です。 ただし、Supply Chain Management がインストールされている場合、特定の状況で倉庫が指定されていない発注書明細行は Supply Chain Management によって許可されるので、この要件は大きではありません。
- 製品受領 (Dataverse での発注書受領) は Supply Chain Management によって管理され、Supply Chain Management がインストールされている場合 Dataverse は作成できません。 Supply Chain Management からの製品受領は、Supply Chain Management から Dataverse へと同期されます。
- Supply Chain Management では過小配送が許可されています。 One GIFSCM ソリューションは、過小配送シナリオで注文中の残りの数量を調整するために、製品受領ライン (または Dataverse での発注書受領製品) が Dataverse で作成または更新されると、在庫仕訳帳行を作成して調整するロジックを追加します。

## <a name="unsupported-scenarios"></a>サポートされないシナリオ

- Field Service は、Supply Chain Management でキャンセルされた発注書に明細行が追加されるのを防ぎます。 Field Service で発注書のシステム ステータスを変更し、その新しい行を Field Service または Supply Chain Management に追加することができます。
- 調達行は両方のシステムの在庫レベルに影響を与えるが、この統合は Supply Chain Management と Field Service での在庫配置を保証しません。 Field Service と Supply Chain Management は両方とも、在庫レベルを更新するその他のプロセスがあります。 これらのプロセスは調達の範囲を外しています。

## <a name="status-management"></a>状態管理

Field Service での発注書の状態は、Supply Chain Management の状態とは異なります。

### <a name="field-service-purchase-order-and-purchase-order-product-statuses"></a>Field Service の発注書と発注書の製品ステータス

| ヘッダー – システムの状態 | ヘッダー - 承認の状態 | 品目の状態 |
|---|---|---|
| <ul><li>ドラフト</li><li>提出済</li><li>キャンセル済</li><li>受領済製品</li><li>請求</li></ul> | <ul><li>Null</li><li>承認済金額</li><li>不採用</li></ul> | <ul><li>保留中</li><li>入庫済</li><li>キャンセル済</li></ul> |

### <a name="supply-chain-management-purchase-order-and-purchase-order-line-statuses"></a>Supply Chain Management の発注書と発注書明細行の状態

明細行の承認の状態は、行ワークフローがある場合にのみ有効になります。

| ヘッダー - ドキュメントの状態 | ヘッダー - 承認の状態 | 明細行の状態 | 明細行の承認状態 |
|---|---|---|---|
| <ul><li>オープン注文 (バックオーダー)</li><li>入庫済</li><li>請求済</li><li>キャンセル済</li></ul> | <ul><li>ドラフト</li><li>確認中</li><li>承認済金額</li><li>不採用</li><li>外部レビューでは</li><li>確定済</li><li>完了</li></ul> | <ul><li>オープン注文 (バックオーダー)</li><li>入庫済</li><li>請求済</li><li>キャンセル済</li></ul> | <ul><li>未送信</li><li>確認中</li><li>承認済金額</li><li>不採用</li></ul> |

状態の列には次のルールが適用されます。

- Supply Chain Management の状態は、Field Service から更新されません。 ただし、Supply Chain Management の発注書の状態が変更された場合は、Field Service の状態が更新される場合があります。
- Supply Chain Management の発注書の変更管理が進行中で、変更の処理中の場合、承認ステータスは *ドラフト* または *確認中* になります。 この場合、Field Service の承認の状態は *Null* に設定されます。
- Supply Chain Management の発注書の承認ステータスが *承認済*、*外部レビュー*、*確認済*、または *[終了済]* に設定されている場合は、Field Service 発注書の承認状態が *承認済* に設定されます。
- Supply Chain Management の発注書の承認状態が *拒否済* に設定されている場合、Field Service 発注書の承認状態が *拒否済* に設定されます。
- Supply Chain Management のドキュメント ヘッダーの状態が *オープン注文 (バックオーダー)* に変更され、Field Service 発注書の状態が *ドラフト* または *キャンセル済* になった場合は、Field Service 発注書の状態が *提出済* に変更されます。
- Supply Chain Management のドキュメント ヘッダーの状態が *キャンセル済* に変更され、Field Service の発注書受領製品が 発注書に (発注書製品を介して) 関連付けられている場合、Field Service システム状態が *キャンセル済* に設定されます。
- Supply Chain Management の発注書明細行の状態が *キャンセル済* の場合は、Field Service の発注書製品の状態が *キャンセル済* に設定されます。 また、Supply Chain Management の発注書明細行の状態が *キャンセル済* から *バックオーダー* に変更された場合は、Field Service の発注書製品品目ステータスが *保留中* に設定されます。

## <a name="sync-with-the-supply-chain-management-procurement-data-on-demand"></a><a id="sync-procurement"></a>Supply Chain Management の調達データオンデマンドとの同期

Supply Chain Management には、契約や割引など、Supply Chain Management の二次プロセスに依存するシナリオを処理する調達データが含まれています。 調達エンジンでは、複雑なルールを使用して、特定の発注書に対して最適な価格を決定します。 デュアル書き込み機能を使用する場合、特に Dataverse から行が作成または更新されたシナリオ、および Supply Chain Management のフォローオン プロセスがトリガされる場合など、2 つの環境でデータのデータが常に同期して維持されるとは限りません。

## <a name="sync-the-procurement-data-from-supply-chain-management"></a>Supply Chain Management からの調達データの同期

1. Dataverse で、**在庫 \> 発注書** に移動します。
2. 新規発注書を作成するには **新規** を選択するか、既存の発注書から行を選択します。
3. 発注書または発注書明細行から。
4. アクション ペインで、**同期** を選択します。

Supply Chain Management によって共有されている Dataverse と Field Service からのすべての列が同期されます。

**同期** 機能を使用できる状況を次に示します。

- Dataverse から同じ行に対して続く複数の変更を行う場合は、**同期** 機能を実行します。
- Dataverse からの変更が 2 回目の変更になるかどうか確信が持てない場合は、**同期** 機能を実行します。
- Supply Chain Management の値の更新に関するエラー メッセージが表示された場合は、Dataverse で **同期** 機能を実行します。

## <a name="cancelling-the-posting-process"></a>転記プロセスのキャンセル

製品受領の転記プロセスが処理中にキャンセルされた場合、二重書き込みは製品受領を Dataverse で作成する場合がありますが、Supply Chain Management では製品受領の行は作成しません。 この状況は、デュアル書き込みでは分散トランザクションがサポートされていないことから発生します。

## <a name="templates"></a>テンプレート

調達関連のドキュメントを統合する場合は、次のテンプレートを使用できます。

| サプライ チェーン マネジメント | Field Service | 説明 |
|---|---|---|
| [発注書ヘッダー V2](mapping-reference.md#183) | msdyn\_Purchaseorders | 次の表に、発注書ヘッダーを表す列を示します。 |
| [発注書明細行エンティティ](mapping-reference.md#181) | msdyn\_PurchaseOrderProducts | このテーブルは、発注書で明細行を示す列を示します。 製品番号が同期に使用されます。 これにより、製品の分析コードを含め、製品を在庫管理単位 (SKU) として識別します。 Dataverse を使った製品統合の詳細については、[統一された製品の体験](product-mapping.md) を参照してください。 |
| [製品受領書ヘッダー](mapping-reference.md#185) | msdyn\_purchaseorderreceipts | 次のテーブルは、Supply Chain Management で製品受領が転記された場合に作成される製品受領 ヘッダーを示しています。 |
| [製品受領書明細行](mapping-reference.md#184) | msdyn\_purchaseorderreceiptproducts | このテーブルは、Supply Chain Management で製品受領が転記された場合に作成される製品受領明細行ヘッダーを示しています。 |
| [発注書明細行によって削除されたエンティティ](mapping-reference.md#182) | msdyn\_purchaseorderproducts | 次のテーブルは、ソフト削除された発注書明細行に関する情報を示しています。 Supply Chain Management の発注書明細行は、変更管理が有効な場合に発注書が確認または承認された場合にのみソフト削除できます。 この行は Supply Chain Management データベースに存在し、**IsDeleted** としてマークされています。 Dataverse にはソフト削除という概念は存在しないので、この情報を Dataverse に同期することが重要です。 これにより、Supply Chain Management でソフト削除された明細行を Dataverse から自動的に削除することができます。 この場合、Dataverse で行を削除するロジックは Supply Chain Management Extende に位置します。 |

[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
