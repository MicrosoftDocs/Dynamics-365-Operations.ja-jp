---
title: コール センターの詐欺警告の設定および使用
description: この記事では、注文が処理されるとき、詐欺の可能性ある情報を顧客サービス担当者に警告するルールを設定する方法について説明します。 疑わしい注文を保留にするために使用される特殊なコードを自動または手動で定義できます。
author: josaw1
ms.date: 05/14/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SalesPostingHistory, MCRHoldCodeTrans
audience: Application User
ms.reviewer: josaw
ms.custom: 79103
ms.assetid: e342af8d-7498-4d20-8483-ab368429c578
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: 212afd594453d3594fdaef9442a7809e4cafbd07
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/03/2022
ms.locfileid: "8885351"
---
# <a name="set-up-and-work-with-call-center-fraud-alerts"></a>コール センターの詐欺警告の設定および使用

[!include [banner](includes/banner.md)]

この記事では、さらなる確認のために詐欺の可能性がある販売注文を保留にする基準とルールを設定する方法について説明します。 不正チェック機能を使用して、販売注文の情報の有効性を決定します。 販売注文の情報が疑わしいように見える場合、組織の不正基準とルールに基づいて、さらなる確認のために保留にすることができます。 この場合、保留がクリアされるまで注文は処理を進めるために倉庫にリリースできません。

> [!NOTE]
> この機能は、コマース コール センター チャネルの販売注文処理にのみ使用できます。

## <a name="turning-on-the-fraud-check-feature"></a>不正チェック機能を有効にする

不正チェック機能を使用するためには、コール センター チャンネルが [定義されている](/dynamics365/unified-operations/retail/set-up-order-processing-options) 場合、チャンネルの **オーダー完了の有効化** オプションを **はい** に設定する必要があります。 オーダー完了が有効な場合、コール センター ユーザーは作成されるすべての販売注文の販売注文ページで **完了** を選択する必要があります。 完了したアクションにより、**販売注文集計** ページが開かれます。 ユーザーは必要な支払データを **販売注文集計** ページに入力した後、**送信** を選択して注文を確定します。 注文が送信されると、不正チェック機能がトリガーされ、システムで有効なルールが自動的に検証されます。

コール センターのユーザーは、**送信** を選択する前に不正確認のため手動で販売注文を保留中にできます。 販売注文の保留を手動で行うには、**販売注文集計** ページで、**保留** \> **手動不正保留** を選択します。 注文を保留にする理由を説明するためのコメントを入力するように求められます。 このコメントは、保留中の注文を確認してその注文をリリースする必要があるかどうかを特定するユーザーにコンテキストを提供するために、[注文保留](/dynamics365/unified-operations/retail/work-with-order-holds) ワークベンチに表示されます。

チャンネルの **オーダー完了の有効化** オプションのコンフィギュレーションに加えて、コール センター パラメーターの不正チェック機能をコンフィギュレーションする必要があります。 **Retail とコマース** \> **チャネル設定** \> **コール センターの設定** \> **コール センター パラメーター** の順に移動します。 **コール センター パラメーター** ページの **保留** タブで **不正チェック** オプションを **はい** に設定します。

**保留** タブでは、不正確認のために手動または自動で保留にする注文に適用される [保留コード](/dynamics365/unified-operations/retail/work-with-order-holds) を定義する必要があります。 **手動不正保留コード** および **不正保留コード** フィールドで保留コードを設定します。 保留ワークベンチで作業するユーザーが自動の保留と手動の保留を簡単にフィルター処理して区別することができるように、2 つの固有の保留コード作成することをお勧めします。

不正チェック機能が効率的に作業するには、**最小スコア** フィールドも設定する必要があります。 システムで定義されているすべての不正条件とルールにはスコアがあります。 不正一致について販売注文が確認されるとき、1 つ以上の一致が見つかった場合、スコアは合計され注文に合計不正スコアが付与されます。 注文の合計不正スコアが **最小スコア** フィールドの値を超える場合、注文は自動的に保留にされます。 必要に応じて電子メール スコア、電話番号スコア、郵便番号のスコア、および拡張郵便番号のスコアを定義するために、**保留** タブのその他のスコア関連のフィールドを使用することができます。 **静的不正データ** ページで定義するとき、いずれかの静的不正基準のスコアを指定しない場合は、**コール センター パラメーター** ページの **保留** タブで指定する既定のスコアを使用することによりスコアを付けることができます。

最後に、不正確認のため手動で注文を保留にする場合、ユーザーがコメントを入力するときに使用するドキュメント タイプを指定するために **不正コメント タイプ** フィールドを使用します。 多くの場合、このフィールドは **注記** に設定されています。

## <a name="defining-fraud-criteria-and-rules"></a>不正基準の定義およびルール

システムは不正確認の注文を保留にするかどうか特定するために 2 つのタイプの不正基準を参照します。

- **静的不正データ** は、ブロックされている番号の一覧に載せられている電話番号または過去の不正なトランザクションに使用されたとしてマークされている電子メール アドレスなど、特定の値を使用します。 静的不正データを設定するには、**Retail とコマース** \> **チャネル設定** \> **コール センターの設定** \> **不正** \> **静的不正データ** の順に移動します。 **静的不正データ** ページで、不正基準を手動でまたはデータのインポートを使用して追加することができます。 スコアは不正情報に関連付けられます。 不正チェック機能が有効である場合は、入力されたすべての販売注文が静的データと比較されます。 注文ヘッダーにリンクされる顧客の請求先住所または配送先住所のいずれかにデータが見つかった場合や、販売注文の明細行のいずれかにリンクされる配送先住所にデータが見つかった場合は、すべての一意の一致スコアが合計され、注文を保留にするかどうかを特定するために **最小スコア** 値と比較されます。

- **不正ルール** はユーザー定義の変数およびそれらの変数に対して定義されている条件で構成されています。 ルールを作成するには、**Retail とコマース** \> **チャネル設定** \> **コール センターの設定** \> **不正** \> **ルール** の順に移動します。 不正ルールにより会社は、複数の条件を評価するために **AND** または **OR** ステートメントが含まれる、より複雑なルール セットを構成することができます。 たとえば、ユーザーは特定の顧客グループに属する顧客および特定の製品を発注した顧客のすべての注文を不正確認のため保留にします。 この場合、顧客および製品を検証するための条件は **ルール** ページで定義され、AND 条件が使用されます。 注文は、両方の条件が true の場合、またはルールに割り当てられているスコア値に、注文が一致するその他のルールのスコア値を加えて、注文の合計不正スコアが **コール センター パラメーター** ページで定義されている **最小スコア** 値を超過する場合のみ保留中となります。

> [!NOTE]
> 複数のルールまたは過剰に複雑なルールは、販売注文が送信されたときにシステムのパフォーマンスに影響を与えることがあります。 不正チェック機能は、大量の静的不正データ エントリと多くの有効なルールを処理するためには最適化されていません。 販売注文の入力時にコール センター ユーザーが **送信** を選択する際、すべてのルールは評価されるという点に注意してください。 ルールは、販売注文ヘッダーとすべての注文明細行に対して評価されます。 より多くのルールおよび、より複数なルール ステートメントは、処理に時間がかかります。 注文で多くの明細行品目、および多くの有効なルールと静的データ エントリがある場合、すべてのデータを確認して検証し、不正スコアを計算する自動プロセスは、パフォーマンスに深刻な影響を与える可能性があります。 この機能を使用する組織は、必ずテストを行い、運用環境に対してルールまたは静的不正基準の変更を適用する前に、注文の送信処理時間が許容可能かどうか確認する必要があります。

## <a name="identifying-orders-that-are-on-hold-for-fraud-review"></a>不正確認のため保留中の注文の識別

コール センター ユーザーは販売注文を送信するとき、注文が不正基準またはルールと一致する場合、またはスコアが最小値を超えた場合に、注文が保留中であることを知らせるメッセージがユーザーに表示されます。 情報提供のみを目的とするため、ユーザーはこのメッセージを閉じることができます。 ユーザーは必要に応じて、この情報を顧客に通信できます。 ビジネスは、ユーザーがこの状況で使用しているプロトコルを特定する必要があります。

注文は保存されますが、**処理禁止** フラグが設定されています。 このフラグは、注文が倉庫にリリースできないことを保証するのに役立ちます。 いつでも、ユーザーは **状態の詳細** ページで販売注文の **処理禁止** フラグの設定を表示できます。 このページは、**すべての販売注文** および **顧客サービス** ページから開くことができます。 また、**不正保留** に対する注文の **状態の詳細** フィールドの値も更新されます。

不正確認のため保留中の注文を表示および管理するには、**Retail とコマース** \> **顧客** \> **注文保留** の順に移動します。 **注文保留** ページで、リストからエントリを選択し、**注文保留** をクリックすると、保留の理由に関する情報を含む詳細ビューが表示されます。 **不正の詳細** クイック タブで、適用された注文とスコアに一致することが検出された体系的な不正基準を表示することができます。 注文が手動保留にされている場合、**メモ** クイック タブの **不正メモ** セクションを参照して注文を保留にしたユーザーによって入力されたコメントを確認できます。

保留注文の操作方法の詳細については、[注文保留](/dynamics365/unified-operations/retail/work-with-order-holds) を参照してください。


[!INCLUDE[footer-include](../includes/footer-banner.md)]