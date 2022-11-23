---
title: 法人別に作業者へのアクセスを制限する
description: この記事では、法人別に作業者のアクセス権を設定する方法について説明します。
author: twheeloc
ms.date: 11/28/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: HcmSharedParameters, HcmPersonnelManagementWorkspace
audience: Application User
ms.custom: 51891
ms.assetid: c7d8f58c-d78a-4035-abbf-2b0ce16109fe
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: fadd2c34d31bbd259255596c06a8e7517f7a774b
ms.sourcegitcommit: cf6b764824bd1cf2c0dde6d37ddd0a7abab87ff0
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/16/2022
ms.locfileid: "9780393"
---
# <a name="restrict-access-to-workers-by-legal-entity"></a>法人別に作業者へのアクセスを制限する

この記事では、法人別に作業者のアクセス権を設定する方法について説明します。

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

従業員は法人で雇用されています。 次にいくつか例を挙げます。

- Aaron Con は USSI の法人で雇用されています。
- Ahmed Barnett は USMF の法人で雇用されています。
- Alicia Thornber は、GLSI および USMF の法人で雇用されています。

会社でのユーザーの役割によっては、すべての法人のすべての従業員を表示するためのアクセスを必要とする場合があります。 または、ユーザーがアクセス権を持つ法人の従業員のみを表示できるよう、制限する必要がある場合があります。 ユーザーが表示できる従業員を制御するには、**Human Resources 共有パラメーター** ページで **作業者情報へのアクセス制限** パラメーターを選択します。

たとえば、ユーザーは **作業者** ページにアクセスでき、USMF 法人にのみアクセスできます。 この場合、ユーザーは上記のリストの従業員に関する次の情報を表示できます:

- 作業者情報へのアクセスを制限する機能が有効になっていない場合、ユーザーは Aaron、Ahmed、および Alicia の情報を表示できます。
- 機能が有効になっている場合、ユーザーは、Alicia と Ahmed の情報のみを表示できます。これは、彼らも USMF 法人で雇用されているためです。

表示される情報は、使用しているアプリケーションによって異なります。

## <a name="dynamics-365-human-resources-stand-alone"></a>Dynamics 365 Human Resources スタンドアロン

作業者情報へのアクセスを制限する機能が有効な場合、制限されたユーザーは、作業者の名前を含む一部のリストに空白の値が表示されます。

たとえば、USMF 法人に対してのみアクセスできるユーザーは、次のような動作を経験します:

- ユーザーは USSI 法人の従業員にアクセスできないので、**有効な職位** リストでは、Aaron の職位の **作業者** 列は空白になります。
- ユーザーが作業者の名前を掘り下げると、空白の **作業者** ページが表示されます。

## <a name="dynamics-365-human-resources-on-finance-infrastructure"></a>Finance インフラストラクチャの Dynamics 365 Human Resources

作業者情報へのアクセスを制限する機能が有効な場合、制限されたユーザーには、一部のリストで作業者の名前が表示されます。

たとえば、USMF 法人に対してのみアクセスできるユーザーは、次のような動作を経験します:

- **有効な職位** のリストでは、**作業者** 列に Aaron の名前が表示されます。 ユーザーが作業者の名前の上にカーソルを合わせると、名前とタイトルだけが表示されます。
- ユーザーが作業者の名前を掘り下げると、空白の **作業者** ページが表示されます。

> [!TIP]
> Finance インフラストラクチャで Dynamics 365 Human resources を使用し、制限されたユーザーに作業者の名前の空白値を表示させる場合、**作業者へのアクセスを制限する** セキュリティ権限を **セキュリティ コンフィギュレーション** ページのユーザー ロールに追加できます。

機能を有効にした後、いくつかの追加手順を実行して、表示を制限する必要がある各ユーザーのアクセス許可を設定する必要があります。

1. **ユーザー** ページで、ユーザーを選択します。
2. ユーザーのロールを選択します。 **組織の割り当て** オプションが使用できるようになります。
3. **組織の割り当て** を選択します。
4. 新しいページで、**特定の組織へのアクセスを個別に付与する** を選択し、ユーザーがアクセスする必要がある組織を選択します。
5. システム ユーザー ロールを含め、ユーザーの持つ他のすべてのロールについて、手順2 ～ 4 を繰り返します。

> [!NOTE]
> ユーザーがアクセスできる法人は、すべてのユーザー ロールで一致している必要があります。
