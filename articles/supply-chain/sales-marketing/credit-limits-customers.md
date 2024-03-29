---
title: 顧客の与信限度額
description: この記事は、Dynamics 365 Supply Chain Management での与信限度額が機能する方法を概観します。
author: Henrikan
ms.date: 09/15/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CustParameters
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: henrikan
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: b4a98b90491093f55ce6974b9b11ff326c0c2f5c
ms.sourcegitcommit: cfe8fbc202c3eb05d894076fdf99e46704f17365
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/15/2022
ms.locfileid: "9015321"
---
# <a name="credit-limits-for-customers"></a>顧客の与信限度額

[!include [banner](../includes/banner.md)]

与信限度額を設定すると、顧客に対して拡張する貸方転記の最大量を指定できます。 与信限度額が指定されている場合、ユーザーがドキュメントの更新を試みると自動的に確認されます。 与信限度額を超えた場合、メッセージがユーザーに表示されます。 この記事では、与信限度額の機能の仕方を概観し、以下の質問に答えます。

-   どの文書とプロセスのために与信限度額を確認できますか。

-   顧客の与信残高を計算する方法をどこでコンフィギュレーションしますか。

-   顧客のクレジット使用残高に関する情報はどこにありますか。

-   顧客の与信限度拡大の請求に ID が必要かどうか、および ID が必要となる与信限度額をどこで指定しますか。

-   与信限度額を超えた場合に警告またはエラーを表示するかどうか、どこで指定しますか。

-   特定の顧客の与信限度額をどのように指定しますか。

-   販売注文の与信限度額をどのように手動で確認しますか。

**どの文書とプロセスのために与信限度額を確認できますか。**

**売掛金勘定パラメーター** フォームを使用して、与信限度額を確認する文書を指定します。 このフォームで変更を加えるには システム管理者 (-SYSADMIN-) セキュリティ ロールのメンバである必要があります。 以下のドキュメントおよびプロセスの与信限度額を確認できます。

-   請求書を転記時の、販売注文の請求書

-   梱包明細を更新時の、販売注文の梱包明細

-   **販売注文** フォームで行を追加する時の、販売注文

-   サービスで作成される時の、販売注文

-   請求書を転記時の、自由書式の請求書

次のオプションのいずれかを設定されている場合、与信限度額は自動的にチェックされます。

-   **売掛金勘定パラメーター** フォームで、**与信限度額のタイプ** フィールドは **なし** 以外に設定されます。 与信限度額はすべての顧客に対して確認されます。

-   **売掛金勘定パラメーター** フォームで、**与信限度額のタイプ** フィールドが **なし** に設定されますが、**顧客** フォームでは顧客に **与信限度確認必須** が選択されます。 与信限度額は、特定の顧客に対してのみ確認されます。

次のドキュメントの与信限度額を確認するには、追加の設定を指定する必要があります。

|    書類                                    |    追加設定                                                                                                             |
|------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
|    自由書式の請求書                         |    [売掛金勘定パラメーター] フォームの [信用格付け] 領域で、[自由書式請求書の与信限度額の確認] を選択します。     |
|    販売注文 (手動入力)            |    [売掛金勘定パラメーター] フォームの [信用格付け] 領域で、[販売注文の与信限度額の確認] を選択します。           |
|    販売注文 (電子的に取得)     |    [売掛金勘定パラメーター] フォームの [AIF] 領域で、[販売注文の与信限度額の確認] を選択します。                     |

**顧客の与信残高を計算する方法をどこでコンフィギュレーションしますか。**

Dynamics 365 をコンフィギュレーションして、以下のいずれかの方法で顧客の与信残高を計算できます。

-   顧客の残高に対する与信限度額を比較します。

-   顧客の残高、梱包明細の量に対する与信限度額を比較します。

-   顧客の残高およびすべてのオープンなトランザクション活動に対する与信限度額を比較します。 これには、梱包明細の量および販売注文の量が含まれます。

**売掛金勘定パラメーター** を使用して、比較する情報を指定します。 このフォームで変更を加えるには システム管理者 (-SYSADMIN-) セキュリティ ロールのメンバである必要があります。 **与信限度額のタイプ** フィールドで、与信限度額の確認を実行するかどうか、また与信限度額チェック時にどのトランザクション情報を含めるかを選択します。 以下のオプションからエラーの原因を選択します。

-   **なし** – 与信限度額を確認しません。 **顧客** フォームの **与信限度確認必須** チェック ボックスをオンにして、特定の顧客に対してこのオプションを上書きできます。 この場合、顧客の残高に対して与信限度額が確認されます。

-   **残高** : 与信限度額が顧客残高と照らしてチェックされます。

-   **残高 + 梱包明細または製品受領書** – 顧客残高および出荷に照らして与信限度額をチェックします。

-   **残高 + すべて** : 与信限度額が顧客残高、出荷、および未処理注文に照らしてチェックされます。

**顧客のクレジット使用残高に関する情報はどこにありますか。**

経過期間スナップショットを作成すると、顧客の残高と与信残高量に関する情報が計算されて保存され、**回収** フォームに表示されます。 **回収** フォームに表示される量には、新しい経過期間スナップショットを作成するまで、すべてのトランザクション活動は含まれない場合があります。 詳細については、「[売掛金勘定の取立と貸方転記](/dynamicsax-2012/appuser-itpro/collections-and-credit-in-accounts-receivable)」を参照してください。

選択したドキュメントに応じて、販売注文、梱包明細、および顧客請求書が更新されると、顧客の残高および与信残高量に関する情報が計算されます。 使用しているドキュメントの量のために与信限度額が超過する場合、メッセージが表示されます。

**顧客の与信限度拡大の請求に ID が必要かどうか、および ID が必要となる与信限度をどこで指定しますか。**

**売掛金勘定パラメーター** フォームを使用して、ID を要求するかどうか、および ID を要求する与信限度量の限度を指定します。
このフォームで変更を加えるには システム管理者 (-SYSADMIN-) セキュリティ ロールのメンバである必要があります。

|    フィールド                                    |    説明                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
|---------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
|    与信枠のある ID を要求     |    法人が与信枠を拡大する顧客に対し、入力する必要がある ID のタイプを選択します。 このフィールドで選択するオプションによって、[顧客] フォームの [政府 ID] フィールドで、どの場合にどのタイプの情報が必要になるかが決まります。[いいえ] – 顧客の与信限度額にかかわらず、政府発行の ID は不要です。     [はい] – 顧客の与信限度額がゼロ以上である場合は、政府発行のライセンス番号またはその他の政府発行 ID が必要です。     [最小値] – 顧客の与信限度額が、このフォームの [限度] フィールドに入力した限度額以上である場合は、政府発行のライセンス番号またはその他の政府発行 ID が必要です。        |
|    限度                                    |    顧客に政府発行のライセンス番号、またはその他の ID が必要となる与信限度額を入力します。    たとえば、「2000」と入力すると、与信限度額が 2,000 以上の顧客には、運転免許証番号などの ID 番号の入力が必要になります。    このフィールドは、[信用のある ID を要求] フィールドで [最小値] を選択した場合に使用できます。                                                                                                                                                                                                                                                                                                                                                                                                                                         |

**与信限度額を超えた場合に警告またはエラーを表示するかどうか、どこで指定しますか。**

**売掛金勘定パラメーター** フォームを使用して、与信限度額を超えた場合に警告またはエラーを表示するかどうか指定します。 この警告またはエラーは、ユーザーが転記情報を入力するときに表示されるか、またはドキュメントが電子サービスで取得される場合にはログに含まれます。 このフォームで変更を加えるには システム管理者 (-SYSADMIN-) セキュリティ ロールのメンバである必要があります。

|    フィールド                                                               |    説明                                                                                                                                                                                                                                                                                                                                                                                        |
|------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
|    ([信用格付け] 領域の) 与信限度額を超えたときのメッセージ     |    与信限度額が超えたことに関するメッセージをユーザーに対して表示する方法を選択します。 次のオプションから選択します。[エラー] – エラー メッセージが表示されます。 通常これにより現在の工程が停止し、プロセスを続行する前に競合を解決する必要があります。     [警告] – 警告メッセージが表示されますが、処理は続行できます。                     |
|    ([AIF] 領域の) 与信限度額を超えたときのメッセージ               |    与信限度額の超過に関するメッセージをログで提供する方法を選択します。 次のオプションから選択します。[エラー] – エラー メッセージが [例外] フォームに表示され、エラーが解決されるまでドキュメントは処理されません。     [警告] – 警告メッセージが [例外] フォームに表示されますが、処理は続行できます。        |

**特定の顧客に対する与信限度額をどのように指定しますか。**

**顧客** フォームを使用して、特定の顧客に対して与信限度額を指定します。 このフォームに変更を加えるには 顧客マスターの管理 (CustCustomersMaintain) の職務権限を割り当てられているセキュリティ ロールのメンバである必要があります。

1.  **売掛金勘定** \> **顧客** \> **すべての顧客** の順にクリックします。 顧客 ID をダブルクリックします。

2.  **顧客** フォームで、アクション ウィンドウの **編集** をクリックします。

3.  **与信限度額** フィールドで、通貨金額を入力します。 この値はゼロ (0) より大きくする必要があり、与信限度額として使用されます。

4.  必要に応じて、**政府 ID** フィールドにライセンス番号またはその他の政府発行の ID を入力します。

> [!NOTE]
> **売掛金勘定パラメーター** フォームで、与信限度額のタイプがたいてい選択されます。 ただし、与信限度額のタイプが **なし** に設定されている場合、顧客の残高に対する顧客の与信限度額を確認するには、**顧客** フォームの **与信限度確認必須** チェック ボックスを選択する必要があります。 与信限度額のタイプの詳細については、このトピックの「どの文書とプロセスのために与信限度額を確認できますか。」を この記事の内容。 

**販売注文の与信限度額を手動でどのように確認しますか。**

場合によっては、顧客の与信限度額を手動で確認する必要があります。 たとえば、販売注文の入力を開始する前に、手動で顧客の与信限度額を確認する場合があります。 **販売注文** フォームを使用して、手動で与信限度額を確認できます。 このフォームに変更を加えるには 販売注文の管理 (SalesOrderMaintain) の職務権限を割り当てられているセキュリティ ロールのメンバである必要があります。

1.  **販売とマーケティング** \> **販売注文** \> **すべての販売注文** の順に移動します。 販売注文をダブルクリックします。

2.  **販売注文** フォームで、アクション ウィンドウの **管理** タブの **与信限度額の確認** をクリックします。


[!INCLUDE[footer-include](../../includes/footer-banner.md)]