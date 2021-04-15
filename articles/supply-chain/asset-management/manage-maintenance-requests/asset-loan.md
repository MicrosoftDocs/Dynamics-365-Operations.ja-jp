---
title: 資産ローン
description: このトピックでは、資産管理でローン資産を登録する方法について説明します。
author: johanhoffmann
ms.date: 10/01/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EntAssetObjectLoanSend, EntAssetObjectLoanListPage, EntAssetObjectLoanReturn, EntAssetObjectLoanInfoPart
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 712f3e7cdfb8d521ae2afb59d90bc5102da53cb7
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/01/2021
ms.locfileid: "5813390"
---
# <a name="asset-loans"></a>資産ローン

[!include [banner](../../includes/banner.md)]

 

会社が内部の場所または顧客から、修理またはメンテナンス ジョブ用の資産を受け取り、それらの場所または顧客に資産を一時的に貸与する場合、資産管理は資産ローンを追跡できます。

## <a name="register-asset-loans-on-a-maintenance-request"></a>メンテナンス要求で資産ローンを登録する

1. **資産管理** \> **共通** \> **メンテナンス要求** \> **すべてのメンテナンス要求** または **有効なメンテナンス要求** を選択します。
2. 資産ローンを登録するメンテナンス要求を選択してから、**編集** を選択します。
3. **要求** ページで、**ローン資産の送信** を選択します。
4. 資産を選択し、返却予定日を入力します。
5. **OK** を選択します。

> [!NOTE]
> - ローン資産は、同じ資産タイプの資産が使用可能な場合にのみ送信できます。
> - 貸与する資産には、**InStorage** など、ローン資産として使用できる資産ライフサイクルの状態が必要です。 資産ローンが登録されると、その資産の資産ライフサイクルの状態が **OnLoan** などに自動的に更新されます。

他の場所または顧客に貸与したすべての資産の一覧を表示するには、**資産管理** \> **共通** \> **資産ローン** \> **すべての資産ローン** を選択します。 資産に対して **終了** チェック ボックスがオンの場合、資産は会社に返却済として登録されています。

![メンテナンス要求の管理](media/06-manage-maintenance-requests.png)

**有効な資産ローン** ページで、会社に返却されていないすべてのローン資産の一覧を表示できます。

## <a name="register-loan-assets-as-returned"></a>ローン資産を返却済として登録する

1. **資産管理** \> **共通** \> **資産ローン** \> **有効な資産ローン** を選択します。
2. 返却済として登録する資産ローンを選択し、**資産ローンの返却** を選択します。
3. **返却済** フィールドで、日時を入力します。
4. **OK** を選択します。
5. **有効な資産ローン** リスト ページを更新し、資産ローンが一覧に表示されなくなったことを確認してください。


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]