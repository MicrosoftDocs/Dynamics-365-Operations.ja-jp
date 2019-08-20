---
title: 一般仕訳帳の処理
description: このトピックでは、一般仕訳帳の処理を容易にすることができ、正確なデータがキャプチャされ内部コントロールが悪影響を受けていないことを確認する手助けとなる Microsoft Dynamics 365 for Finance and Operations の機能について説明します。
author: ShylaThompson
manager: AnnBe
ms.date: 09/24/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerJournalSetup, LedgerJournalTable
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 15721
ms.assetid: b4b406fa-b772-44ec-8dd8-8eb818a921ef
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: d7efd250428f7675b96674dd02e3aeccefe653fe
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/01/2019
ms.locfileid: "1839234"
---
# <a name="general-journal-processing"></a>一般仕訳帳の処理

[!include [banner](../includes/banner.md)]

このトピックでは、一般仕訳帳の処理を容易にすることができ、正確なデータがキャプチャされ内部コントロールが悪影響を受けていないことを確認する手助けとなる Microsoft Dynamics 365 for Finance and Operations の機能について説明します。  

## <a name="journal-names"></a>仕訳帳名

設定する重要な分野の 1 つは、仕訳帳名です。 会社間、見越計上調整、エラーの修正など、目的ごとに特定の仕訳帳名を定義することをお勧めします。 目的ごとにデータ入力を簡単かつ安全にするために、それぞれの仕訳帳名をカスタマイズできます。 

**仕訳帳名** ページで、次の要素を設定できます :

-   **ワークフローの承認** ー 内部コントロールを向上するために、合計借方金額などの基準に基づいて、確認および承認ステップの物質能力制限を設定する仕訳帳ワークフローを定義します。 一般仕訳帳のワークフローを **総勘定元帳ワークフロー** ページに設定します。
-   **既定値** – 相手勘定、通貨、財務分析コードの既定値を選択します。
-   **仕訳帳コントロール** – 会社と勘定タイプの制限、および区分値を設定できます。 

**例**

仕訳帳名は調整のためのみにに使用されます。 この場合、すべての会社で **元帳** 勘定タイプのみが有効であるように指定できます。 

[![仕訳帳コントロール勘定タイプ](./media/journal-control-account-types1.png)](./media/journal-control-account-types1.png)

仕訳帳名は、特定の区分のみまたは主勘定の範囲に対して使用できます。 

[![仕訳帳コントロール区分](./media/journal-control-segment1.png)](./media/journal-control-segment1.png)

**自動取消** オプションは、一般仕訳帳で使用できます。 たとえば、次の図に示すように、実際のドキュメントがまだ処理されていない見越計上の調整が行われます。
[![一般仕訳帳の取り消し](./media/general-journal-reversing1.png)](./media/general-journal-reversing1.png) 

仕訳帳入力のための Microsoft Excel アドインは、自動化の追加のレベルを提供し、データ入力をより簡単にします。 **Excel で明細行を開く** アクションは、**一般仕訳帳** および **仕訳伝票** ページで使用できます。 

**定期処理仕訳帳** ページで、繰返しの仕訳帳を仕訳処理の自動化に設定できます。 

伝票テンプレートはいつでも使用できます。 **一般仕訳帳** ページでは、**保存** および **伝票テンプレートの選択** アクションは、伝票明細行の **機能** の **仕訳伝票** ページにあります。

## <a name="related-setup"></a>関連する設定
次の設定は、一般仕訳帳に固有のものではありませんが、データ入力が正しいデータで簡単であることを確認するのに役立ちます。

### <a name="main-account"></a>主勘定

主勘定の設定には、一般仕訳帳の処理にさまざまなオプションが提供されます :

-   **DC/CRの条件** ー 主勘定が借方もしくは貸方トランザクションに限定される場合はこのオプションを使用します。 設定は、仕訳帳を検証するか、または転記したときに確認されます。

-   **既定の相手勘定**
-   **中断** – は、すべての会社または特定の会社や法人のデータ入力用の主勘定を中断します。
-   **手動入力を許可しない** – ユーザーが仕訳帳の勘定に手動で値を入力することを防ぎます。
-   **既定 / 通貨の検証**
-   **法人の上書き** – この設定は、定義された会社や法人固有のものです :
    -   **規定 / 売上税の検証**
    -   **既定の分析コード** ー **固定なし** または **固定値** **固定値**はこの主勘定のすべての転記が、常に**固定**として設定されているどの分析コード値でも使用できるようにします。
-   **転記検証**
    -   **ユーザーの検証** – このオプションは、主勘定に転記することが許可されるユーザーを管理します。
    -   **転記タイプの検証** – このオプションは、主勘定に対して使用できる転記タイプを管理します。

### <a name="accounting-structures-and-advanced-rules-structures"></a>勘定構造および詳細ルール構造

勘定構造および詳細ルールの構造は、財務報告に必要とされるデータおよびパフォーマンスの追跡が、一般仕訳帳の処理とドキュメンテーションの間にキャプチャされることを確認するために非常に重要です。 勘定構造および詳細ルール構造により、データ入力経験のカスタマイズが可能になります。 それぞれの状況に該当する財務分析コードに対してのみデータ入力を許可し、必要かつ正確なデータを常にキャプチャするという要件を適用することもできます。

詳細については、次のトピックを参照してください。
- [計画: 勘定科目表](plan-chart-of-accounts.md)。 
- [仕訳帳の詳細なルールの作成](tasks/create-advanced-rules-journals.md)
- [テンプレートを使用した仕訳入力の作成](tasks/create-journal-entry-template.md)
- [仕訳帳の作成および検証](tasks/create-validate-journals.md)
- [定期処理仕訳帳の転記](tasks/post-periodic-journals.md)
- [元帳配賦仕訳帳の処理](tasks/process-ledger-allocation-journal.md)

## <a name="simulate-posting"></a>転記をシミュレーション
**検証**メニューで、ほとんどの仕訳帳の**シミュレート転記**を検索できます。 **検証**機能を使用して仕訳帳を検証すると、システムは特定のエラー条件について仕訳帳をテストします。 **シミュレート転記**を使用すると、転記中に実行されるすべてのプロセスが実際に転記されずに実行されます。 その後、表示される転記メッセージの確認、エラーの修正を行い、**転記**メニューをクリックして、仕訳帳を転記します。 

**シミュレート転記**はバッチ処理では使用できません。 ただし、バッチの転記をシミュレートするために使用可能なコードがあり、開発者はコードを拡張してその機能を追加することができます。  
