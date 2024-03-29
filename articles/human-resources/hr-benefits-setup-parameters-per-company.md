---
title: 会社ごとの給付金管理パラメーターのコンフィギュレーション
description: この記事では、Microsoft Dynamics 365 Human Resources で会社ごとに給付金管理パラメーターを構成する方法について説明します。
author: twheeloc
ms.date: 8/24/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BenefitWorkspace, HcmBenefitSummaryPart
audience: Application User
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-12-07
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 2f3f8625a8ebbe6812d2f051649ff2a608ed4b54
ms.sourcegitcommit: 66d129874635d34a8b29c57762ecf1564e4dc233
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2022
ms.locfileid: "9323901"
---
# <a name="configure-benefits-management-parameters-per-company"></a>会社ごとに給付金管理パラメータを構成する


給付金を提供する組織ごとに、給付金確認メールの設定を構成する必要があります。

## <a name="configure-confirmation-email-settings"></a>確認メール設定の設定

1. **福利厚生管理** ワークスペースの **設定** で、**人事管理パラメーター** を選択します。

2. **福利厚生の管理** タブで、次のフィールドの値を指定します: 

   | フィールド | 説明 |
   | --- | --- |
   | **確認メールを送信する** | この機能がオンになっている場合は、**従業員セルフ サービス** の給付金登録エクスペリエンスから確認メールが従業員に送信されます。 |
   | **確認メール テンプレート** | 登録の確認を送信するときに使用する組織のメール テンプレートを選択します。 テンプレートを選択しない場合は、次の一般的なメールが送信されます。<br><br>%EmployeeFirstName%、<br><br>おめでとうございます。 給付金の登録が正常に完了しました。<br><br>よろしくお願いいたします。<br><会社/組織名> 給付金。 |
   | **既定のメール送信者アドレス** | 確認メールを送信するときに使用するメール アドレス。 |

3. **保存** を選択します。

[!INCLUDE[footer-include](../includes/footer-banner.md)]
