---
title: Dataverse の企業概念
description: このトピックでは、Finance and Operations と Dataverse 間の企業データの統合について説明します。
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 08/04/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2019-07-15
ms.openlocfilehash: 189d1b8a68f8457d32d656fefeb6cc2a332a3b22
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/09/2021
ms.locfileid: "5560252"
---
# <a name="company-concept-in-dataverse"></a>Dataverse の企業概念

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]


Finance and Operations では、*企業* の概念は、法的コンストラクトとビジネス コンストラクトの両方です。 また、データのセキュリティと可視性の境界でもあります。 ユーザーは常に単一の会社のコンテキストで作業し、データのほとんどは会社によってストライプされます。

Dataverse は、同等の概念を持っていません。 最も近い概念は、主にユーザー データのセキュリティと可視性の境界である *事業単位* です。 この概念は、企業概念と同じ法的またはビジネス上の意味を持ちません。

事業単位と企業は同等の概念ではないため、Dataverse 統合を目的として 1 対 1 (1:1) のマッピングを強制することはできません。 ただし、ユーザーは既定でアプリケーションと Dataverse で同じ行を表示する必要があるため、Microsoft では cdm\_Company という Dataverse に新たなテーブルを導入しています。 このテーブルは、アプリケーションの企業テーブルと同等です。 行の可視性はアプリケーションと Dataverse 間で同等に、すぐに使用できることを保証するために、Dataverse のデータで次の設定をお勧めします。

+ デュアル書き込みが有効になっている Finance and Operations の企業の行ごとに、関連付けられた cdm\_Company の行が作成されます。
+ cdm\_Company の行が作成され、デュアル書き込みが有効になると、同じ名前の既定の事業単位が作成されます。 既定のチームは、その事業単位に対して自動的に作成されますが、事業単位は使用されません。
+ 同じ名前を持つ別の所有者チームが、作成されます。 また、事業単位にも関連付けられています。
+ 既定では、作成されて、Dataverse にデュアル書き込みされた行の所有者は、関連付けられた事業部にリンクされている 「DW 所有者」 チームに設定されます。

次の図では、Dataverse のデータ設定の例を示します。

![Dataverse のデータ設定](media/dual-write-company-1.png)

この構成により、USMF 社に関連する行は、Dataverse の USMF 事業単位にリンクされているチームが所有します。 したがって、事業単位レベルの可視性に設定されたセキュリティ ロールを通じて、その事業単位にアクセスできるユーザーは、これらの行を表示できるようになります。 次の例は、チームを使用してこれら行への正しいアクセスを提供する方法を示しています。

+ 「営業マネージャー」のロールは、「USMF セールス」チームのメンバーに割り当てられます。
+ 「営業マネージャー」のロールを持つユーザーは、自分が所属する同じ事業単位のメンバーである任意の取引先企業の行にアクセスできます。
+ 「USMF セールス」チームは、前述の USMF 事業単位にリンクされています。
+ したがって、「USMF セールス」チームのメンバーは、Finance and Operations の USMF 会社テーブルから来た「USMF DW」ユーザーが所有するアカウントを確認できます。

![チームの使用方法](media/dual-write-company-2.png)

前の図に示すように、事業単位、企業、およびチーム間の 1:1 マッピングは、出発点に過ぎません。 この例では、新しい「ヨーロッパ」の事業単位が DEMF と ESMF の両方の Dataverse にて手動で作成されます。 この新しいルートの事業単位は、デュアル書き込みとは無関係です。 ただし、関連するセキュリティー ロールの **親 / 子 BU** にデータの可視性を設定することにより、DEMF および ESMF の両方のアカウント データに対する「EUR 営業」チームのメンバーにアクセスできるよう使用できます。

最後に、デュアル書き込みによって、どの所有者チームに行の割り当てが決定されるかについて説明します。 この動作は、cdm\_Company 行の **既定の所有チーム** 列で制御します。 cdm\_Company 行がデュアル書き込みに有効となっている場合、プラグインは関連付けられた事業単位と所有者チームを自動的に作成し (存在しない場合)、**既定の所有チーム** 列を設定します。 管理者は、この列を別の値に変更できます。 ただし、テーブルがデュアル書き込みを有効にしている限り、管理者は列をクリアできません。

> [!div class="mx-imgBorder"]
![既定の所有チーム列](media/dual-write-default-owning-team.jpg)

## <a name="company-striping-and-bootstrapping"></a>企業のストライピングとブートストラップ

Dataverse 統合は、企業の識別子を使用してデータをストライプすることにより、企業パリティをもたらします。 次の図に示すように、すべての企業の固有のテーブルは、cdm\_Company テーブルと多対1 (N:1) の関係を持つよう拡張されます。

> [!div class="mx-imgBorder"]
![企業の固有テーブルと cdm_Company テーブル間の N:1 関係](media/dual-write-bootstrapping.png)

+ 行の場合、企業が追加、保存された後で、値が読み取り専用になります。 したがって、ユーザーは正しい企業を選択する必要があります。
+ 企業データを持つ行のみが、アプリケーションと Dataverse 間のデュアル書き込みの対象となります。
+ 既存の Dataverse データによって、管理者主導のブートストラップ エクスペリエンスがまもなく利用可能になります。


## <a name="autopopulate-company-name-in-customer-engagement-apps"></a>Customer Engagement アプリに会社名を自動入力する

Customer Engagement アプリで会社名を自動入力するには、いくつかの方法があります。

+ システム管理者は、**詳細設定 > システム > セキュリティ > ユーザー** に移動することによって、既定の会社を設定できます。 **ユーザー** フォームを開き、**組織情報** セクションで **会社をフォーム上の既定** 値に設定します。

    :::image type="content" source="media/autopopulate-company-name-1.png" alt-text="組織情報セクションで既定の会社を設定します。":::

+ **事業単位** レベルの **SystemUser** テーブルに対する **書き込み** アクセス権がある場合は、**会社** ドロップダウン メニューから会社を選択することにより、任意のフォームで既定の会社を変更できます。

    :::image type="content" source="media/autopopulate-company-name-2.png" alt-text="新しいアカウントで会社名を変更します。":::

+ 複数の会社のデータへの **書き込み** アクセス権がある場合は、別の会社に属する行を選択して既定の会社を変更することができます。

    :::image type="content" source="media/autopopulate-company-name-3.png" alt-text="行を選択すると、既定の会社が変更されます。":::

+ システム コンフィギュレーターまたは管理者で、会社データをカスタム フォームに自動入力する場合、[フォーム イベント](https://docs.microsoft.com/powerapps/developer/model-driven-apps/clientapi/events-forms-grids) を使用できます。 JavaScript リファレンスを **msdyn_/DefaultCompany.js** に追加し、次のイベントを使用します。 **アカウント** フォームなど、すぐに利用できるフォームを使用することができます。

    + フォームの **OnLoad** イベント: **defaultCompany** 列を設定します。
    + **会社** 列の **OnChange** イベント: **updateDefaultCompany** 列を設定します。

## <a name="apply-filtering-based-on-the-company-context"></a>会社コンテキストに基づくフィルター処理の適用

カスタム フォーム、または標準フォームに追加されたカスタム ルックアップ列の会社コンテキストに基づいてフィルター処理を適用するには、フォームを開き、**関連レコードのフィルター処理** セクションを使用して、会社フィルターを適用します。 この設定は、指定された行の基礎となる会社に基づくフィルター処理が必要となる各ルックアップ列に対して行う必要があります。 次の図に **アカウント** の設定を示します。

:::image type="content" source="media/apply-company-context.png" alt-text="会社コンテキストの適用":::



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]