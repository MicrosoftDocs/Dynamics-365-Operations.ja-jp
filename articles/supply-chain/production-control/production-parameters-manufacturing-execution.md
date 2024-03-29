---
title: 製造実行の生産パラメーター
description: この記事では、製造実行における生産パラメータの設定に関する情報について説明します。
author: johanhoffmann
ms.date: 06/16/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: JmgProdParameters
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 6d440a0d0d95fe93ed633fa588e1c3a193757d9d
ms.sourcegitcommit: 28a726b3b0726ecac7620b5736f5457bc75a5f84
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/29/2022
ms.locfileid: "9070382"
---
# <a name="production-parameters-in-manufacturing-execution"></a>製造実行の生産パラメーター

[!include [banner](../includes/banner.md)]

この記事では、製造実行における生産パラメータの設定に関する情報について説明します。

**製造実行** モジュールは、主に製造会社を対象としています。 生産ジョブやプロジェクトでの時間と品目の消費を登録するために使用できます。 ジョブ登録の製造実行モジュールの使用を開始する前に、最初に生産プロセスで登録をいつどのように転記するかを定義するさまざまな生産パラメータを設定する必要があります。 生産パラメータの設定は、在庫管理、生産管理、および原価計算に影響します。

作業者が生産ジョブに登録する前に、**生産パラメータ** ページのすべての設定を注意深く考慮する必要があります。 **生産管理** &gt; **設定** &gt; **製造実行** &gt; **生産パラメータ** の順にクリックします。 会社がマルチサイト機能を使用する場合は、サイトごとに異なる生産パラメータを設定することができます。 **生産** モジュールと統合したパラメータは、**生産パラメータ** ページの次のタブで設定できます:

- **一般** – 製造実行の生産ジョブにおける一般のパラメータ設定。
- **開始** – 生産工程の開始時に使用されるパラメータ。
- **工程** – 生産プロセス中の生産工程および工程に関するフィードバックに適用されるパラメータ。
- **完了レポート** – 製造オーダーの最後の工程の完了後、品目を報告する際に使用されるパラメータ。
- **数量の検証** – 製造オーダーの開始数量およびフィードバック数量を検証するために使用されるパラメータ。

## <a name="types-of-production-jobs"></a>生産ジョブのタイプ
**工程** タブで、**ジョブ登録** ページの登録する必要がある生産ジョブのタイプを選択します。

通常、作業者は設定ジョブとプロセス ジョブを登録します。 ただし、ジョブのスケジューリングが適用されている場合は、製造オーダーの処理時にも作業者が登録する必要がある他のジョブ タイプを選択できます。 たとえば、配送ジョブで登録を要求することができます。

> [!IMPORTANT]
> 関連するすべてのジョブ タイプが選択されていることを確認してください。 それ以外の場合は、**ジョブ登録** ページで登録できるジョブが現れない場合があります。 あなたの選択は、**工順グループ** ページ (**生産管理** &gt; **設定** &gt; **工順** &gt; **工順グループ**) にある **設定** タブの **ジョブ管理** 列の選択と一致する必要があります。

工順グループで **ジョブ管理** が選択されている場合、このジョブ タイプは、[製造実行] の完了報告時に製造オーダーの完了として報告されます。 **ジョブ管理** が選択されているすべてのジョブ タイプで工程が完了報告されると、[製造実行] の工程も完了報告されます。

> [!NOTE]
> 一部のジョブ タイプは生産仕訳帳から手動で報告できます。 この場合、ジョブ タイプには **ジョブ管理** を選択しますが、**生産パラメータ** ページの **工程** タブでは、登録するジョブ タイプを選択しないでおきます。

## <a name="bom-consumption-and-picking-list-journals"></a>BOM 消費とピッキング リスト仕訳帳
在庫管理が効率的であることを保証するのに役立つため、部品表 (BOM) の一貫した設定が重要です。 たとえば、[製造実行] で BOM 消費パラメータが正しく設定されていない場合、材料が在庫から 2 回差し引かれたり、まったく差し引かれなかったりする場合があります。

**生産パラメータ** ページは、自動 BOM 消費は 3 つのステージで設定されます:

- 生産の開始時。 **開始** タブでこのステージを設定します。
- 工程が完了されるときの生産プロセス中。 **工程** タブでこのステージを設定します。
- 製造オーダーが完了済と報告されるとき。 **完了レポート** タブでこのステージを設定します。

各ステージでは、**自動 BOM 消費** フィールドを使用して、製造オーダーの品目をピッキングするための 3 つの方法のいずれかを選択できます。

- **部品消費ルール** – このオプションは、**生産** モジュールの BOM で定義されたオプションと組み合わせて使用されます。 **製造管理** &gt; **製造オーダー** &gt; **すべての製造オーダー** をクリックします。 **すべての製造オーダー** ページで、一覧で [製造オーダー] を選択し、次に [アクション ペイン] で、**BOM** をクリックします。 **BOM** ページにある **設定** タブの **部品消費ルール** フィールドで、次のオプションのいずれかを選択します:

  - **開始**
  - **完了**
  - **手動**
  - 空白 – (オプションは選択されません。)
  - **場所で利用可能**

    [製造実行] で、**開始** タブの **自動 BOM 消費** フィールドに **部品消費ルール** が選択された場合、BOM の **開始** に設定されているすべての品目は、工程開始時に在庫から差し引かれます。 **場所で利用可能** オプションは、倉庫管理プロセス (WMS) が有効になっている製品に使用されます。 部品消費ルールを選択する場合、原原材料ピッキングの倉庫作業が完了すると、材料がフラッシュされます。 この部品消費ルールを使用する BOM 明細行が倉庫にリリースされ、材料が生産入庫の場所で利用可能になると、材料もフラッシュされます。

    > [!NOTE]
    > 製造実行の **開始** タブで **部品消費ルール** フィールドが設定されている場合、**工程** タブまたは **完了レポート** タブのいずれかで同じ原則を選択する必要があります。この要件は、材料が製造オーダーの部品消費ルールとして **完了** を使用する BOM の在庫から差し引かれることを保証するのに役立ちます。 **工程** タブまたは **完了レポート** タブで同じ部品消費ルールが選択されていない場合、材料は在庫から 2 回差し引かれることがあります。

- **常時** – このオプションをステージで選択する場合、そのステージで在庫が常に差し引かれます。 たとえば、生産の材料が製造オーダーの開始時に差し引かれます。 この設定では、**工程** および **完了レポート** タブで **なし** を選択する必要があります。 この要件は、品目が在庫から 2 回差し引かれるのを防ぐのに役立ちます。
- **なし** – ステージでこのオプションを選択すると、その段階で BOM 消費は発生しません。 たとえば、3 つのすべてのタブ (**開始**、**工程**、および **完了レポート**) で **しない** を選択する場合、材料は在庫から手動で差し引かれなければなりません。

> [!IMPORTANT]
> 生産パラメータの設定を慎重に検討し、**生産パラメータ** ページのさまざまなタブで選択されたパラメータが互いに矛盾しないことを確認してください。

次の各例で、さまざまな BOM 消費原則をサポートするパラメータの設定について示します。 パラメータは、製造実行の **生産パラメータ** ページに設定されます。

### <a name="example-1-backflushing-on-operations"></a>例 1 : 工程でのバックフラッシュ

工程での品目の完了報告時にピッキング リスト仕訳帳および BOM 品目の消費を生成する必要がある場合は、以下の設定を使用します。

| タブ                | フィールド                          | 設定                             |
|--------------------|--------------------------------|-------------------------------------|
| 開始              | オンラインで開始を更新           | **ステータス** または **ステータス + 数量** |
| 開始              | 自動 BOM 消費      | **許可しない**                           |
| Operations         | 自動 BOM 消費      | **常時**                          |
| 完了レポート | 自動 BOM 消費      | **許可しない**                           |
| 完了レポート | オンラインで完了レポートを更新 | **ステータス + 数量**               |

### <a name="example-2-backflushing-on-production"></a>例 2 : 生産でのバックフラッシュ

製造オーダーでの品目の完了報告時にピッキング リスト仕訳帳および BOM 品目の消費を生成する必要がある場合は、以下の設定を使用します。

| タブ                | フィールド                          | 設定                             |
|--------------------|--------------------------------|-------------------------------------|
| 開始              | オンラインで開始を更新           | **ステータス** または **ステータス + 数量** |
| 開始              | 自動 BOM 消費      | **許可しない**                           |
| Operations         | 自動 BOM 消費      | **許可しない**                           |
| 完了レポート | 自動 BOM 消費      | **常時**                          |
| 完了レポート | オンラインで完了レポートを更新 | **ステータス + 数量**               |

### <a name="example-3-flushing-principle"></a>例 3 : 部品消費ルール

BOM 品目の部品消費ルールの設定に従ってピッキング リスト仕訳帳および BOM 品目消費を生成する必要がある場合は、以下の設定を使用します。

| タブ                | フィールド                          | 設定                |
|--------------------|--------------------------------|------------------------|
| 開始              | オンラインで開始を更新           | **ステータス + 数量**  |
| 開始              | 自動 BOM 消費      | **部品消費ルール** |
| Operations         | 自動 BOM 消費      | **部品消費ルール** |
| 完了レポート | 自動 BOM 消費      | **許可しない**              |
| 完了レポート | オンラインで完了レポートを更新 | **ステータス + 数量**  |

### <a name="example-4-deduction-of-materials-during-startup-of-a-production-order"></a>例 4 : 製造オーダーの開始時の材料の控除

生産の開始時にピッキング リスト仕訳帳および BOM 品目の消費を生成する必要がある場合は、以下の設定を使用します。

| タブ                | フィールド                          | 設定                             |
|--------------------|--------------------------------|-------------------------------------|
| 開始              | オンラインで開始を更新           | **ステータス + 数量**               |
| 開始              | 自動 BOM 消費      | **常時**                          |
| Operations         | 自動 BOM 消費      | **許可しない**                           |
| 完了レポート | 自動 BOM 消費      | **許可しない**                           |
| 完了レポート | オンラインで完了レポートを更新 | **ステータス** または **ステータス + 数量** |

このセクションで前述されている選択に基づいて、ピッキング リスト仕訳帳は製造オーダー プロセスのさまざまなステージで転記されます:

- 工程の開始時
- 工程での数量フィードバックの報告時
- 製造オーダーでの品目の完了報告時

### <a name="example-5-manual-bom-consumption"></a>例 5 : 手動の BOM 消費

次の設定は、常に手動で材料を在庫から差し引く必要がある場合に使用できます。 この場合、ピッキング リスト仕訳帳は転記されません。


|        タブ         |             フィールド              |         設定         |
|--------------------|--------------------------------|-------------------------|
|       開始        |      オンラインで開始を更新      | <strong>ステータス</strong> |
|       開始        |   自動 BOM 消費    | <strong>許可しない</strong>  |
|     Operations     |   自動 BOM 消費    | <strong>許可しない</strong>  |
| 完了レポート |   自動 BOM 消費    | <strong>許可しない</strong>  |
| 完了レポート | オンラインで完了レポートを更新 | <strong>ステータス</strong> |



[!INCLUDE[footer-include](../../includes/footer-banner.md)]