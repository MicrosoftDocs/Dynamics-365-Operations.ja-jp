---
title: 共有パラメーターのコンフィギュレーション
description: 職位レコードなど、会社間で共有されるのレコードの共有パラメーターを設定する必要があります。 この記事は、法人間に人事管理パラメーターを設定する方法を説明します。
author: andreabichsel
manager: tfehr
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-human-resources
ms.technology: ''
ms.search.form: HcmSharedParameters, HcmPersonnelManagementWorkspace
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 51891
ms.assetid: c7d8f58c-d78a-4035-abbf-2b0ce16109fe
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 297141ab17660533b441629ccdfc624bbcb9c82b
ms.sourcegitcommit: 6affb3316be757c99e1fe9c7c7b312b93c483408
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/17/2021
ms.locfileid: "5467292"
---
# <a name="configure-shared-parameters"></a>共有パラメーターのコンフィギュレーション

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

職位レコードなど、会社間で共有されるのレコードの共有パラメーターを設定する必要があります。 この記事は、法人間に人事管理パラメーターを設定する方法を説明します。

職位レコードなどの一部のレコード タイプは、会社間で共有されます。 これらのレコードに対して、共有パラメータを設定する必要があります。 たとえば、法人間で人事管理パラメーターを設定する場合、**人事管理、パラメータを共有** ページを使用します。 

**人事管理の共有パラメーター** ページで、パラメータは機能に基づいて領域にグループ化されます。 

### <a name="previously-released-functionality"></a>以前にリリースされた機能
**ID** タブで、ページに表示される ID 番号を表す ID タイプを選択する必要があります。 作業者の ID 情報を入力する前に、ID タイプを設定する必要があります。 社会保障番号、国民 ID 番号、外国人 ID 番号、および個人の ID コードに関する情報が **ID タイプ** ページで管理されます。 新しい ID タイプを定義する、または既存のタイプの一覧を確認するには、**人事管理** &gt; **リンク タブ** &gt; **設定** &gt; **ID タイプ** の順にクリックします。 簡単なコードと説明を入力できます。 

### <a name="if-youre-using-dynamics-365-human-resources"></a>Dynamics 365 Human Resources を使用している場合
**ID** タブで、ページに表示される ID 番号を表す ID タイプを選択する必要があります。 作業者の ID 情報を入力する前に、ID タイプを設定する必要があります。 社会保障番号、国民 ID 番号、外国人 ID 番号、および個人の ID コードに関する情報が **ID タイプ** ページで管理されます。 新しい ID タイプを定義する、または既存のタイプの一覧を確認するには、**人事管理** &gt; **設定** &gt; **ID タイプ** の順にクリックします。 簡単なコードと説明を入力できます。 

**番号順序** タブで、次のレコードに使用する番号順序を選択できます: 個人番号、職位、ユーザー要求 ID、I-9 ドキュメント、申請者、ディスカッション、福利厚生のID、および従業員のアクション (このレコード タイプが有効な場合)。 番号順序およびコードを管理するには、**番号順序** リスト ページを使用します。 このページを検索するには、ページの検索機能を使用します。 

**職位** タブで、新しい職位が既定で割り当てに使用できるかどうかを指定します:

-   **常時** – 職位の作成時に新しい職位に作業者を割り当てることができます。 職位を作成すると、**職位** ページの **概要** タブ上の **割り当てに使用可能** 日時が、自動的に作成日時に設定されます。
-   **なし** – 職位の作成時に新しい職位に作業者を割り当てることはできません。 このオプションを選択する場合、新しい各職位が使用できるように **職位** ページを開き、作業者の割り当てを有効にするのに **一般** タブの **割り当てに使用可能** 日付を入力する必要があります。


[!INCLUDE[footer-include](../includes/footer-banner.md)]