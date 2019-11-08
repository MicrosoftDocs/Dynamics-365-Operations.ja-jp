---
title: Dynamics 365 Talent Core HR (2018 年 12 月 6 日) の新機能および変更された機能
description: このトピックでは、Microsoft Dynamics 365 Talent - Core HR の新機能または変更された機能について説明します。
author: Darinkramer
manager: AnnBe
ms.date: 12/07/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2018-12-06
ms.dyn365.ops.version: Talent
ms.openlocfilehash: bb43745b5a52c10b2d54480005d9d4e5ca6dc5bf
ms.sourcegitcommit: 75db3b75d35d27034f9b56e7119c9d0cb7666830
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/03/2019
ms.locfileid: "2550254"
---
# <a name="whats-new-or-changed-in-dynamics-365-talent---core-hr-december-6-2018"></a>Dynamics 365 Talent Core HR (2018 年 12 月 6 日) の新機能および変更された機能

[!include [banner](includes/banner.md)]

**ビルド 8.1.2071**

このトピックでは、Core HR の新機能または変更された機能について説明します。


## <a name="platform-update-22-for-finance-and-operations"></a>Finance and Operations のプラットフォーム更新プログラム 22

### <a name="export-up-to-1-million-rows-to-excel"></a>最大 100 万行を Excel にエクスポート

Excel へのエクスポート機能は、Talent のグリッドから最大 100 万行をエクスポートできるように構成されました。以前の 10,000 行の制限から大幅に上昇しました。 

### <a name="restyled-personalization-toolbar"></a>個人用設定ツールバーの再編成

個人用設定ツールバーが Finance and Operations のプラットフォーム更新 22 で再編成され、ユーザーが Talent でエクスペリエンスを簡単にカスタマイズできるようになりました。 次の変更が加えられました。 

-  各個人用設定ツールの名前がアイコンと共に表示されるようになったため、ユーザーが使おうと思っているツールをすばやく認識できます。
-  現在のツールを使用する方法についての説明も表示され、必要な個人用設定を行う方法を理解するのに役立ちます。  
-  ツールバーの一番左にある特定の領域にドラッグ アンド ドロップすることで、個人用設定ツールバー全体を画面内で移動できます。 これにより、ユーザーは以前はツールバーによって見えにくかった要素をカスタマイズできます。   

### <a name="optimized-is-one-of-filtering-experience"></a>「次の値のいずれか」のフィルタリング結果を最適化

「次の値のいずれか」フィルター演算子は、フィルター ウィンドウおよびグリッド ヘッダーのドロップダウン リストを使用する場合にほとんどのフィールドで使用できます。 この演算子により、複数の値に基づいてフィールドをフィルター処理できます。 「次の値のいずれか」演算子の新機能と向上したエクスペリエンスは Finance and Operations のプラットフォーム更新 22 で利用可能です。 詳しくは、[「次の値のいずれか」のフィルタリング結果の最適化](https://docs.microsoft.com/business-applications-release-notes/October18/dynamics365-finance-operations/improved-isoneof-filtering)をご覧ください。

### <a name="paste-lists-from-excel-into-filter-fields-with-the-is-one-of-operator"></a>"次の値のいずれか" 演算子を使って Excel からフィルター フィールドにリストを貼り付け

一部のタスクでは、Talent でデータのフィルター処理に使用する値の一覧が Excel に表示されることがあります。 たとえば、人事管理ユーザーは、システムで追加の調査を必要とする一連の従業員をレポートから特定している可能性があり、このユーザーが Excel から Talent のフィルター フィールドに直接リストをコピーできると最適な場合があります。

Finance and Operations のプラットフォーム更新 22 以降では、フィルター ウィンドウおよびグリッド列フィルターの「次の値のいずれか」演算子が、フィルター フィールドに直接貼り付けることができるように、Excel からコピーされたリストを認識するようになりました。 これには、Excel のさまざまな行と列からコピーされた値のコレクションが含まれます。 この機能の詳細については、["次の値のいずれか" 演算子を使用して Excel からフィルター フィールドに一覧を貼り付ける](https://docs.microsoft.com/business-applications-release-notes/October18/dynamics365-finance-operations/paste-filter-lists-from-excel)を参照してください。

## <a name="in-preview"></a>プレビュー

### <a name="configure-uk-payroll-integration-between-talent-and-dayforce"></a>Talent と Dayforce 間の UK 給与統合のコンフィギュレーション

Talent および Ceridian Dayforce の統合は、英国のプレビューで利用可能です。 詳細については、次のトピックを参照してください。[Talent と Dayforce の間での給与統合のコンフィギュレーション](https://docs.microsoft.com/dynamics365/unified-operations/talent/configure-payroll-integration)

## <a name="coming-soon"></a>間もなく公開

### <a name="leave-and-absence-future-leave-and-forecasting-leave-balances"></a>休暇と欠勤: 未来の休暇と休暇残高の予測

従業員が休暇を予測し、現在の休暇残高に影響を与えずに将来の休暇時間要求ができるようにするための変更が行われたため、休暇残高の表示方法も変更されました。 

現在表示されている使用可能な残高は、現在までの見越しおよび承認されたすべての休暇申請を含む申請に対して利用可能な休暇の量です。 

予測機能がリリースされると、表示されている残高は、現在までの見越額および申請を含めて、現在の休暇の残高に変更されます。 従業員およびマネージャーの両方が、**休暇**カードと**残高休暇**ウィンドウにある従業員およびマネージャー セルフ サービスで更新された残高を参照できます。 **人員**ワークスペースと従業員の**割り当て済の休暇計画**ウィンドウにある更新済みの残高は HR マネージャーが参照できます。

## <a name="other-changes"></a>その他の変更 

### <a name="termination-code-is-not-populated-to-the-worker-position-assignment-record"></a>退職コードは、作業者の職位割り当てレコードには設定されません

退職処理中に職位割り当てレコードの理由コードを入力する変更が実装されています。

### <a name="validation-for-personnel-number-being-in-use-needs-additional-details"></a>追加情報のために必要な使用中の個人番号の検証

新しい番号が生成できない時、問題をわかりやすくするため、番号順序が使用中の場合、追加情報が表示されます。
 
### <a name="attachments-buttons-not-available-for-workers"></a>作業者は添付ファイルボタンを使用できません

添付ファイルを修正するための変更が行われました。 作業者に新しい添付ファイルを追加する時、作業者ウィンドウの情報ボックスが開いている場合は**新規**および**編集**ボタンが使用可能になりました。 

## <a name="known-issues"></a>既知の問題

### <a name="mapping-errors-in-the-integration-with-finance"></a>Finance との統合のマッピング エラー

次の問題は、Talent を Finance と統合するための現在のテンプレートで識別されています。 新しいテンプレートは、間もなく公開され、作成されたすべての新しい統合プロジェクトに適用されます。 既存の統合プロジェクトのために、タスク マッピングを更新できます。 更新されたマッピングについては、次の表を参照してください。 

>[!NOTE]
> ジョブ職位から職位親ジョブ割り当てタスクはデータが統合されていません。 この問題は現在調査中です。 現在のマッピングに回避策はありません。 

部門から作業単位タスクは、次のマッピングの更新が必要です。

| 既存のソース フィールド          | 新規ソース フィールド |
| -------------------------------|------------------|
| cdm_description (説明)  | cdm_name (名前)  |

追加のマッピングも追加する必要があります。 最後の**なし**フィールドを選択して、次のマッピングを追加します。

| ソース フィールド                   | 出力先フィールド    |
| -------------------------------|----------------------|
| cdm_description (説明)  | NAMEALIAS (NAMEALIAS)|

更新されたマッピングは、次のようになります。

![部門から作業単位タスク](./media/DepartmentMapping.png)


ジョブからジョブ詳細タスクへは、次のマッピングの更新が必要です。

| 既存のソース フィールド          | 新規ソース フィールド                   |
| -------------------------------|------------------------------------|
| cdm_name (名前)                | cdm_description (説明)      |
| cdm_name (名前)         | cdm_jobdescription (職務明細書)|


更新されたマッピングは、次のようになります。

![ジョブからジョブ詳細タスク](./media/JobMapping.png)

作業者から作業タスクへは、次のマッピングの更新が必要です。

| 既存のソース フィールド                 | 新規ソース フィールド                               |
| --------------------------------------|------------------------------------------------|
| cdm_emailaddress1 (電子メール アドレス 1)   | cdm_primaryemailaddress (主要な電子メール アドレス |
| cdm_telephone1 (電話1)          | cdm_primarytelephone (代表電話)       |

性別フィールドの変換は、更新する必要があります。 性別の**fn** (機能) マップを選択し、次の値のマッピングを更新します。

| Common Data Service 値   | Finance and Operations 値 | | ------------|------------------ -----------| | 75440000    | 男性                         | | 75440001    | 女性                       | | 75440002    | なし                         | | 75440003    | 一般                  |

更新されたマッピングは、次のようになります。

![作業者から作業者タスク](./media/WorkerMapping.png)

![性別フィールドの変換](./media/WorkerTransform.png)

