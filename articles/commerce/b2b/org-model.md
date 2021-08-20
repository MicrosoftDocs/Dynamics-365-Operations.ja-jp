---
title: B2B 組織の組織モデリング階層の作成
description: このトピックでは、企業間 (B2B) 組織の組織モデリング階層を作成する方法について説明します。
author: josaw1
ms.date: 01/20/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: RetailOperations
audience: Application User, IT Pro
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: retail
ms.author: josaw
ms.search.validFrom: 2021-01-31
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 0602e0f4e36beda06f47314f40b59967272469755d1b9959432e86f407c098e7
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/05/2021
ms.locfileid: "6738080"
---
# <a name="create-org-modeling-hierarchies-for-b2b-organizations"></a>B2B 組織の組織モデリング階層の作成

[!include [banner](../../includes/banner.md)]

このトピックでは、Microsoft Dynamics 365 Commerce で企業間 (B2B) 組織の組織モデリング階層を作成する方法について説明します。

Commerce 本部では、取引先組織は顧客および顧客階層のエンティティで表されます。 取引先組織とそのユーザーは顧客として表され、顧客階層を使用してこれらの顧客を関連付けします。

取引先が B2B e コマース サイトへの参加を要求すると、次のアクションが実行されます。

- システムに 2 つの新しい顧客レコードが作成されます : 取引先組織の場合は **組織タイプ** 顧客レコード、依頼者の場合は **担当者タイプ** 顧客レコード (申請を行った取引先組織のユーザー)。
- **顧客 \> 顧客階層** の下に新しい顧客階層レコードが作成されます。 このレコードには、次のヘッダー プロパティがあります :

    - **顧客階層 ID** - 顧客階層の固有 ID です。 この ID では、Commerce 本部の [Commerce] 共有パラメータで定義されている番号順序が使用されます。
    - **名前** - オンボード リクエストで指定した取引先組織の名称です。
    - **目的** - このプロパティは、**B2B 組織** の定義済の値に設定されます 。
    - **組織** - 取引先の顧客 ID です。

顧客階層レコードの詳細を次に示します :

- 申請者の顧客レコードは顧客階層に関連付けられます。
- 管理者ロールは申請者に関連付けられます。

管理者が B2B サイトの取引先組織にユーザーを追加すると、Commerce 本部にユーザーごとの新しい顧客レコードが作成されます。 この顧客レコードは、取引先の関連する顧客階層レコードにも追加され、"ユーザー"のロールを持ちます。

> [!NOTE]
> ほとんどの場合、階層内のすべての顧客レコードの対応するプロパティ値は一致している必要があります。 たとえば、すべての取引先ユーザーは共通する製品価格とする必要があるため、価格グループと関連する構成は一致している必要があります。 ただし、この整合性はシステムが適用します。 したがって、関連する Commerce 本部のユーザーは、特定の階層内のすべての顧客のプロパティ値と構成が一致している必要があります。

Commerce 本部のユーザーは、階層内のすべての顧客レコードのプロパティ値を並べて表示することができます。 ドロップダウン メニューのタブ名を選択して、関連する顧客レコードのプロパティを選択します。 ユーザーは、このビューからプロパティの値を直接確認したり、編集したりすることができます。 または、管理者の顧客レコードからすべての値をすべてのユーザーの顧客レコードに適用する場合は、顧客階層の詳細で **上書き** を選択します。

## <a name="additional-resources"></a>追加リソース

[B2B eコマース サイトの設定](set-up-b2b-site.md)

[B2B eコマース サイトでのビジネス パートナー ユーザーの管理](manage-b2b-users.md)

[B2B eコマース サイト用の顧客アカウントの支払方法の構成](payment-method.md)

[B2B eコマース サイトの製品数量制限の設定](quantity-limits.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]