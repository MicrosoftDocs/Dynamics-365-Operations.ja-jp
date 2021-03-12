---
title: 定期売買の発生
description: サービスの定期売買では、手数料トランザクションを請求した日付に続く期間に、収益を手動で見越計上します。
author: ShylaThompson
manager: tfehr
ms.date: 04/30/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMASubscriptionGroup
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: f6d0d6c25cc8a19f5ebea3477cd2c957876752fd
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/15/2021
ms.locfileid: "4966083"
---
# <a name="accruing-subscriptions"></a>定期売買の発生 

[!include [banner](../includes/banner.md)]


サービスの定期売買では、手数料トランザクションを請求した日付に続く期間に、収益を手動で見越計上します。

発生期間は、定期売買手数料に対して設定した請求期間に対して作成されるもので、定期売買の期間コードに基づいています。

未収収益は、見越計上およびリバースが可能です。

## <a name="reverse-accruals-of-credit-amounts"></a>貸方金額の見越計上

請求した定期売買金額を貸方転記する場合は、見越計上金額を 2 つの方法で取り消すことができます。

  - トランザクションの訂正票提案を作成する前に、各未収収益トランザクションを個別に取り消すことができます。 これが手動の方法です。 (手動)

  - 訂正票が転記された日または見越計上の元の転記日に未収金額を取り消すことができます。

詳細については、[定期売買パラメータ (フォーム)](https://technet.microsoft.com/library/aa619615.aspx) を参照してください。

## <a name="setup-requirements"></a>要件の設定

収益を見越計上するには、次のようにデータ要件が満たされていることを確認します。

## <a name="account-setup"></a>勘定の設定

**プロジェクト** モジュールで **仕掛品 - 定期売買** および **未収収益 - 定期売買** 勘定を設定する必要があります。

未収収益を転記すると、**仕掛品 - 定期売買** 勘定が見越計上金額で借方転記され、**未収収益 - 定期売買** 勘定が見越計上金額で貸方転記されます。

## <a name="set-up-accounts-for-accrual-of-subscription-revenue"></a>定期売買収益の見越計上に使用する勘定の設定

1.  **プロジェクト管理および会計** \> **設定** \> **転記** \> **元帳転記の設定** の順にクリックします。

2.  **収益勘定** タブをクリックし、アカウントを設定するため **仕掛品 - 定期売買** または **未収収益 - 定期売買** を選択します。

## <a name="subscription-group-setup"></a>定期売買グループの設定

定期売買の見越計上を可能にするには、**未収収益** チェック ボックスをオンにします。 これは、定期売買に関連付けられたグループの **定期売買グループ** フォームにあります。 **サービス管理** \> **設定** \> **サービスの定期売買** \> **定期売買グループ** の順にクリックします。

## <a name="enable-revenue-accrual-on-a-subscription-group"></a>定期売買グループに対する収益の見越計上の有効化

1.  **サービス管理** \> **設定** \> **サービスの定期売買** \> **定期売買グループ** の順にクリックします。

## <a name="periods"></a>期間

請求期間コードを設定する必要があります。 請求と同じ期間内に収益を見越計上しない場合は、発生期間も設定する必要があります。

次の表に、各請求期間に対して設定できる発生期間の概要を示します。

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>請求期間</p></th>
<th><p>発生期間</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>年</strong></p></td>
<td><ul>
<li><p><strong>年</strong></p></li>
<li><p><strong>四半期</strong></p></li>
<li><p><strong>月</strong></p></li>
<li><p><strong>日</strong></p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><strong>四半期</strong></p></td>
<td><ul>
<li><p><strong>四半期</strong></p></li>
<li><p><strong>月</strong></p></li>
<li><p><strong>日</strong></p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p><strong>月</strong></p></td>
<td><ul>
<li><p><strong>月</strong></p></li>
<li><p><strong>日</strong></p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><strong>週</strong></p></td>
<td><ul>
<li><p><strong>日</strong></p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p><strong>日</strong></p></td>
<td><ul>
<li><p><strong>日</strong></p></li>
</ul></td>
</tr>
</tbody>
</table>

請求期間の設定は、定期売買グループ全体の設定の必須部分です。 定期売買グループに発生期間も設定するかどうかを選択できます。 定期売買グループの発生期間を設定すると、この期間が **期間コード** フィールドに表示されます。 このフィールドは、定期売買の収益を見越計上する際に **未収の定期売買収益** フォームにあります。 ただし、発生期間は定期売買グループに関する必須の情報ではありません。


> [!NOTE]
> <P>次のパスを使用して<STRONG>未収の定期売買収益</STRONG>フォームを開きます。 <STRONG>サービス管理</STRONG>&gt;<STRONG>定期処理</STRONG>&gt;<STRONG>サービスの定期売買</STRONG>&gt;<STRONG>未収の定期売買収益</STRONG>の順にクリックします。</P>


## <a name="transactions"></a>トランザクション

未収収益を転記するときに作成される元帳トランザクションの数を制御できます。 定期売買で、元帳トランザクションを合計または行ごとのどちらとして作成するかを定義します。

## <a name="specify-the-level-of-posting-details-to-display-for-accrued-transactions"></a>未収トランザクションに表示する転記詳細のレベルの指定

1.  **プロジェクト管理と会計** \> **設定** \> **プロジェクト管理および会計パラメーター** の順にクリックします。

2.  **請求書** フィールドの **財務** タブで、**合計** または **明細行** を選択します。


## <a name="see-also"></a>参照

[未収の定期売買収益](accrue-subscription-revenue.md)

  


