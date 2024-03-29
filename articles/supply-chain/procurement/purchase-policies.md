---
title: 購入ポリシーの概要
description: この記事は、購入ポリシーに関する情報を提供します。 購入ポリシーは、要求プロセスを制御するルールのコレクションです。 購入ポリシーは調達管理者が組織の戦略購買の要求に対応するポリシー構造を作成することによって自分の調達戦略を実行できるように助けます。
author: GalynaFedorova
ms.date: 07/25/2019
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: PurchReqSourcingPolicyRule, SysPolicy, SysPolicyListPage, PurchReqControlRule, RequisitionReplenishCatAccessPolicyRule, PurchReApprovalPolicyRule, RequisitionReplenishControlRule, PurchReqControlRFQRule
audience: Application User
ms.reviewer: kamaybac
ms.custom:
- "11614"
- intro-internal
ms.assetid: 729a304d-0f3f-4ccb-bd5b-46ee0976c57f
ms.search.region: Global
ms.author: gfedorova
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 56d8f11d1bb53ef580e33ea43c84369c9e7fc0cc
ms.sourcegitcommit: 0f33f7b7d34d4f9c31ae0faf06a7a5c04b0195a4
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/24/2022
ms.locfileid: "9804903"
---
# <a name="purchasing-policies-overview"></a>購入ポリシーの概要

[!include [banner](../includes/banner.md)]

この記事は、購入ポリシーに関する情報を提供します。 購入ポリシーは、要求プロセスを制御するルールのコレクションです。 購入ポリシーは調達管理者が組織の戦略購買の要求に対応するポリシー構造を作成することによって自分の調達戦略を実行できるように助けます。

購入ポリシーは、ポリシー ルールで構成されます。 ポリシー ルールを定義する場合は、最初にルール タイプを選択します。 その後、ルールの設定、開始日と終了日を定義してルール タイプのルールを作成します。  

たとえば、管理者はポリシーを作成し、**カタログ ポリシー** ルール タイプを選択し、そのポリシーにカタログ ポリシー ルールを追加します。 このカタログ ポリシー ルールは、冒険カタログが内部調達に使用されることを指定します。 購入ポリシーが特定の組織に関連づけられると、その組織の従業員が要求を作成するときに冒険カタログが表示されます。

## <a name="assigning-policies-to-organizations"></a>組織へポリシーを割り当てる
ポリシーが有効になる前に、組織に関連付ける必要があります。 購入ポリシーは、**調達内部統制** の階層目的に関連付けられます。 したがって、購入ポリシーは **調達内部統制** の階層目的を持つ組織の階層にのみ適用できます。 また、CompanyInfo テーブルの法人のフラット リストから組織を選択できます。 これらの法人は、「会社」としてポリシー フレームワークに指定されます。

## <a name="determining-which-rule-to-apply"></a>適用されるルールの決定
購入ポリシーのコンフィギュレーション方法によっては、複数のルールが組織内のユーザーに影響を与える可能性があります。 次の例では、購入ポリシーをコンフィギュレーションし、トランザクションの発生時にポリシーをどのように適用するかを指定する方法について説明します。

### <a name="example-1-simple-purchasing-policy-configuration"></a>例 1: 簡易購入ポリシーのコンフィギュレーション

小規模で比較的簡単な組織では、法人が購入ポリシーを設定できます。そして、[会社] 組織階層のみを使用します。  

Fabrikam は小規模企業で、組織間で購入のニーズの差異があまりありません。 購入ルールは、組織の法人間でのみ違っています。 たとえば、Fabrikam カナダの従業員 と Fabrikam 米国の従業員は、異なるカタログや異なる仕入先から商品やサービスを購入します。 したがって、Fabrikam は法人レベルの購入ポリシーを設定します。  

Fabrikam は、2 種類の購入ポリシーを作成します。 ポリシー A は、米国の法人 1111 に適用されます。 ポリシー B は、カナダの法人 2222 に適用されます。 法人 1111 の従業員が購買要求を作成するとき、ポリシー ルールはポリシー A から派生されます。たとえば、従業員が見る製品カタログは、ポリシー A のカタログ ポリシー ルールで指定されます。  

法人 2222 の従業員が購買要求を作成するとき、ポリシー ルールはポリシー B から派生されます。  

**注記:** 法人 1111 の従業員が法人 2222 の従業員に代わって品目を購入した場合、法人 2222 (ポリシー B からのポリシー ルール) に対して指定されるポリシー ルールが適用されます。

### <a name="example-2-complex-purchasing-policy-configuration"></a>例 2: 複雑な購入ポリシーのコンフィギュレーション

前の例では、すべての購入ルールは 1 つの組織階層、この場合 [会社] 組織階層に定義されています。 ただし、複雑な組織では複数の組織階層のポリシーを定義する場合があります。  


Contoso は要求プロセスを制御するのに複雑な購入ルールが必要な大規模な会社です。 Contoso は 2 つの組織階層のルールを定義します。部門およびグローバル購買コントロール。  

ポリシー 123 は、Sales UK の 部門 (販売部門) の組織階層に対して定義されます。 ポリシー 123 で、購買要求コントロール ルールは最小注文数量が適用される制限を指定します。 このルールで、**最小注文数量制限の実施** オプションが選択されます。  

ポリシー 456 は、販売およびマーケティング部門のグローバル購入コントロールの組織階層に対して定義されます。 ポリシー 456 で、購買要求コントロール ルールは最小注文数量制御が適用されないように指定されます。 このルールで、**最小注文数量制限の実施** オプションが選択解除されます。  

Samは、Sales UK つまり Contoso 社の英国オフィスの販売部門で働いています。 部門の組織階層およびグローバル購入コントロールの組織階層の両方のポリシーが康介の部門に適用されます。 Sam が購買要求を作成すると、システムが適用するポリシーを決定します。 システム管理者は、購入ポリシー パラメータを設定して、購買ポリシーが次の優先順位で適用されるように指定します。

1.  グローバル購買コントロール
2.  部門。
3.  法人

したがって、ポリシー 456 は康介が作成した購買要求に適用され、購買要求には最小注文数量は必要ではありません。

## <a name="policy-rules"></a>ポリシー ルール
### <a name="catalog-policy-rule"></a>カタログ ポリシー ルール

カタログ ポリシー ルールは、ユーザーが購買要求を作成するときに表示される調達カタログを決定します。 ユーザーが別のユーザーに代わって製品を注文するアクセス許可を付与されている場合、要求は、依頼者の法人および作業単位に対して定義されているカタログ ポリシー ルールを使用して、表示されるカタログを決定します。 カタログ ポリシー ルールを定義する前に、購買カタログを作成して公開する必要があります。

### <a name="category-access-policy-rule"></a>カテゴリ アクセス ポリシー ルール

カテゴリ アクセス ポリシー ルールは、ユーザーが購買要求を作成したときにどのカテゴリにアクセス許可があるかを決定します。 ルールが指定されていない場合は、すべての調達カテゴリを購買要求に追加できます。

1.  カテゴリに親組織のカテゴリにアクセスするポリシー ルールを適用するには **親ルールを含める** オプションをオンにします。
2.  **使用可能なカテゴリ** のウィンドウで、ルールが適用されるカテゴリを選択します。 カテゴリを選択すると、階層内のより高いすべてのカテゴリが **選択されたカテゴリ** 一覧に追加されます。
3.  選択したカテゴリのすべてのサブカテゴリにルールを適用するには **サブカテゴリを含める** オプションをオンにします。

### <a name="category-policy-rule"></a>カテゴリ ポリシー ルール

カテゴリ ポリシー ルールは、ユーザーが各カテゴリの仕入先を選択する方法を定義します。 また、入庫および請求プロセスの条件を定義します。

### <a name="re-approval-rule-for-purchase-orders"></a>発注書の再承認ルール

再承認ルールは、発注書を変更するときに再承認の要求の基準を定義するオプションのルールです。 "発注書の再承認が必要" 条件がワークフローで設定されている場合、選択したフィールドは発注書ワークフローで評価されます。

> [!NOTE]
> 変更管理が有効になっている承認済購買注文が変更されると、勘定配布が常にリセットされます。 したがって、特定のフィールドが変更されたときに発注書の再承認を回避する場合は、Accounting distribution.changed フィールドを、再承認のために選択されたフィールドとして含めないようにする必要があります。 

### <a name="purchase-requisition-rfq-rule"></a>購買要求 RFQ ルール

購買要求 RFQ ルールは、購買要求明細行の見積依頼 (RFQ) を要求する基準を定義するルールです。 明細行が条件を満たす場合、"非公式 RFQ" または "公式 RFQ" のタイム スタンプは要求明細行に表示されます。

### <a name="purchase-requisition-control-rule"></a>購買要求管理ルール

**消費** タイプの要求に対する購買要求管理ルールは、オプションのルールです。 このタイプのルールを作成すると、さまざまなタブのオプションを設定できます。

-   **ワークフローの送信** タブでは、承認のために送信される要求に対して要求明細行に入力する必要があるフィールドを構成できます。
-   **注文数量** タブで、特定の条件下で購買要求に必要なフィールドをコンフィギュレーションできます。 また、注文数量を適用できます。
-   **日付** タブで、決算日が要求日と同じかどうかを設定できます。
-   **アドレス** タブで、ユーザーが購買要求に適用するシステムで新しい住所を作成することが許可されるかを定義できます。

### <a name="requisition-purpose-rule"></a>要求目的ルール

要求目的ルールは、特定の法人で許可される要求目的のタイプを決定するオプションのルールです。 別の目的がこのルールで指定されない限り、要求が作成された時にその要求には自動的に **消費** の目的があるようになります。

### <a name="replenishment-category-access-policy-rule"></a>補充のカテゴリ アクセス ポリシー ルール

補充のカテゴリ アクセス ポリシー ルールは、要求目的が **補充** のとき、特定の法人の要求需要を達成するために使用できる製品を決定するオプション ルールです。

### <a name="replenishment-control-rule"></a>補充管理ルール

補充管理ルールは、請求の目的が **補充** のときに、承認のために送信する要求の明細行のフィールドに対して入力する必要のあるフィールドを定義するオプション ルールです。

### <a name="purchase-order-creation-and-demand-consolidation-rule"></a>発注書作成および需要集約ルール

購買発注の作成と需要の統合ルールは、承認された購買要求から発注書が生成されたときに使用するポリシー ルールを定義します。 このタイプのルールを作成すると、さまざまなタブのオプションを設定できます。

-   **発注書の分割** タブで、別の発注書に購買要求明細行を分割する基準を定義できます。
-   **価格/割引のコピー** タブで、発注書を作成するときに価格協定をいつ再計算するか定義できます。
    -   **売買契約がない場合のみ** – 該当する売買契約または基準価格がない場合にのみ、価格および割引は購買要求から転送されます。 売買契約または基準価格が品目または仕入先に対して存在する場合、価格と割引は売買契約または基準価格に基づき再計算され、発注書に適用されます。 特に指定のない限り、これは既定の動作です。
    -   **常に** – 価格および割引は購買要求から常に転送されます。

    定義された価格/割引の転送のルールに関係なく、要求者が個々の購買要求明細行の価格および割引を変更できるようにすることができます。 この機能を有効にする場合は **購買要求明細行ごとに手動での上書きを許可する** オプションをオンにします。
-   **品目の説明のコピー** タブで、RFQ から発生した品目説明を請求から転送できます。
-   **価格許容範囲** タブで、調達カタログの品目の価格が増加する際に、確認プロセスで承認済購買要求の処理に使用する価格許容範囲ルールを定義します。 購買要求上の行品目の正味金額が、購買要求が承認される時間と発注書が作成される時間の間に増加できる最大量を設定します。 正味金額は次の式を使用して計算されます。(\[数量 x (単価 – 割引) ÷ 価格単位\] + 購買雑費) × (100 – 割引率) ÷ 100 設定した価格許容範囲を超える購買要求明細行は、手動で処理されます。 **エラー処理** タブで構成したルールにより、購買要求明細行の処理方法が決まります。
-   **エラー処理** タブで、仕入先エラーまたは価格許容範囲エラーのために発注書の作成時に検証が失敗する場合に、購買要求に適用される処理ルールをコンフィギュレーションできます。 次のいずれかのオプションを選択します。
    -   **アクションなし** – **承認済購買要求のリリース** ページに購買要求明細行が残ります。 購買要求明細行の状態は **承認済** に残ります。 ただし、発注書が購買要求明細行に対して生成する前に、エラーを解決する必要があります。
    -   **購買要求明細行のキャンセル** – 購買要求明細行が取り消されます。 依頼者がまだ明細行品目を要求する場合は、依頼者はキャンセルされた明細行に新しい購買要求を作成できます。
    -   **新しい購買要求明細行の作成** – 購買要求明細行が取り消されます。 検証に失敗した購買要求明細行のみを含む、新しい購買要求が生成されます。 新しく生成された購買要求は、**ドラフト** 状態になります。 検証エラーが解決されると、これらの購買要求はレビューのために再送信できます。 明細行がキャンセルされ、失敗した購買要求明細行のために新しい購買要求が生成されると、購買要求明細行の作成者は通知を受けます。
-   **発注書の手動作成** タブで、購買要求を手動で処理する必要があるか、または自動的に発注書に変換されるかどうかを決定するパラメーターを定義できます。 パラメータは、内部カタログの品目、外部カタログの品目、またはカタログ以外の品目に適用できます。 次のいずれかのオプションを選択します。
    -   **手入力の発注書** – すべての購買要求の発注書を手動で作成します。
    -   **発注書の自動作成** – すべての承認済購買要求の発注書を自動で作成します。 手動の発注書作成では、購買要求は保持されません。
    -   **以下の条件を除き、発注書を自動的に作成** – 定義した基準に一致する購買要求の発注書を手動で作成します。 承認された他のすべての購買要求は、自動的に発注書に変換されます。 **以下の条件を除き、発注書を自動的に作成** を選択すると、手動処理で保持される承認済購買要求明細行を指定するため、調達カタログおよび仕入先を追加できます。 オプションは、内部カタログの品目、外部カタログの品目、およびカタログ以外の品目に適用できます。 調達カテゴリを選択すると、その調達カテゴリの下位カテゴリも選択されます。 特定のタイプの購買要求明細行に **すべて** オプションを選択し、手動処理の際にその明細行タイプのすべての明細行を保持します。

    発注書生成のバッチ ジョブ実行時に、自動的に発注書が承認済購買要求から生成されるようにする場合、**自動発注書作成をバッチ ジョブとして実行** オプションをオンにします。 このオプションは手動処理が必要ない購買要求にのみ適用されます。 自動発注書生成をバッチ ジョブとして実行すると、リソースの制約が少ない時間にこの活動をスケジューリングできます。 購買要求明細行で **必要な前払額** オプションが選択されている場合、承認済購買要求を手動処理として保持するには、**前払の要求の設定時** オプションを選択します。 手動処理のために保持された購買要求はフィルタ処理でき、前払を要求するそれらの購買要求明細行のみを表示することができます。
-   **需要連結** タブで、手動で処理された購買要求を購買要求連結の対象にできるかを決定するパラメーターを定義できます。 パラメータは、内部カタログの品目、外部カタログの品目、またはカタログ以外の品目に適用できます。 次のいずれかのオプションを選択します。
    -   **需要連結を許可しない** – 承認済購買要求明細行に需要連結の資格はありません。 このオプションは既定でオンになり、発注書の作成に手動処理が必要な購買要求明細行にのみ適用されます。
    -   **需要連結を常に許可する** – すべての承認済購買要求明細行に需要連結の資格があります。 **メモ:** **需要連結** タブの **需要連結を常に許可する** オプションを選択していても、**発注書の手動作成** タブの **発注書の自動作成** オプションを選択すると、すべての購買要求が手動処理に保持されます。
    -   **以下の条件の場合に需要連結を許可する** – 承認済購買要求明細行が需要連結に適用できるかどうかを決定する条件を定義します。 購買要求明細行のタイプごとに、調達カテゴリ、および仕入先によって条件を設定できます。 **以下の条件の場合に需要連結を許可する** を選択すると、購買要求明細行のタイプごとに、調達カテゴリ、および仕入先によって条件を設定できます。 調達カテゴリを選択すると、その調達カテゴリの下位カテゴリも選択されます。 特定の行タイプの **すべて** オプションを選択すると、その行タイプのすべての購買要求明細行に需要連結の資格があります。






[!INCLUDE[footer-include](../../includes/footer-banner.md)]