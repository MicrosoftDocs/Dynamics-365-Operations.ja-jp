---
title: 個人情報の編集
description: この記事では、従業員およびマネージャー セルフ サービスで個人情報を編集する方法について説明します。
author: twheeloc
ms.date: 08/26/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: HRMParameters, EssWorkspace
audience: Application User
ms.custom: 51941
ms.assetid: 2cfb061a-a616-4bf9-9d98-9cde00039eec
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-03-19
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: d7e78873d0995334ac80ac22e8058b7fe0bc31ac
ms.sourcegitcommit: a58dfb892e43921157014f0784bd411f5c40e454
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/04/2022
ms.locfileid: "8686125"
---
# <a name="edit-personal-information"></a>個人情報の編集


[!INCLUDE [PEAP](../includes/peap-2.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

個人情報は、**従業員セルフ サービス** ワークスペース の Dynamics 365 Human Resources で編集できます。

編集できる個人情報には、次のものが含まれます。

- 住所
- 連絡先の詳細
- 個人の連絡先
- ID 番号
- 支払方法
- Human Resources で使用される画像

>[!NOTE]
>ビジネス用連絡先の詳細など、特定のタイプの個人情報を編集できない場合があります。 詳細については、[個人情報の編集の制限](hr-employee-self-service-restrict-editing.md)を参照してください。

**グローバル アドレス帳パラメーター** ページで設定されたパラメーターによって、個人情報を参照できるロールが決まります。

1. Human Resources で、**従業員セルフサービス** を選択します。

2. **個人の詳細の編集** を選択します。

3. 住所を変更するには、**住所** タブをクリックします。加えた変更は、**人事管理** のワークスペースに表示され、HR に警告します。

    - 新しい住所を追加するには、**追加** を選択します。
    - 既存の住所を編集するには、住所を選択し、**編集** を選択します。
    - マップを表示するには、**マップ** を選択します。
    - 連絡先を追加または削除するには、**詳細オプション** を選択して、**詳細** を選択します。 **連絡先情報** で、必要に応じて **追加** または **削除** を選択し、フィールドを編集します。
    - タイムゾーンと場所を設定するには、**詳細オプション** を選択肢、**詳細** を選択します。 **一般** で、必要に応じてフィールドを編集します。

4. 連絡先の詳細を変更するには、**連絡先の詳細** タブをクリックします。電話、メール、ソーシャルメディア リンクなど、さまざまなタイプの連絡先情報を提供できます。 連絡先詳細はプライマリとして設定できますが、各タイプのうち 1 つのみをプライマリとして設定できます。

    - 新しい連絡先情報を追加するには、**追加** を選択します。 必要に応じて、情報を編集します。
    - 既存の住所を編集するには、項目を選択してから、**編集** を選択します。 必要に応じて、情報を編集します。
    - 連絡先の詳細をプライベートとして設定するには、**詳細** を選択し、**プライベート** トグルを **はい** に設定します。 **OK** を選択します。
      >[!NOTE]
      >管理者が環境内の **(プレビュー) 従業員が特定の目的で住所や連絡先情報の追加または編集を制限する** 機能を有効にした場合、**詳細** ボタンは使用できません。 詳細については、[個人情報の編集の制限](hr-employee-self-service-restrict-editing.md)を参照してください。
  
5. 個人の連絡先を変更するには、**個人の連絡先** タブを選択します。緊急連絡先、受益者、および扶養家族を指定できます。 連絡先は、個人または組織にできます。 **厚生管理** 機能では、個人の連絡先情報を使用します。 詳細については、[個人連絡先の適格性オプションコンフィグレーション](hr-benefits-setup-contact-eligibility-options.md) をご覧ください。

6. ID 番号 (社会保障番号など) を変更するには、**ID 番号** タブを選択します。組織で承認ワークフローを設定している場合、変更によって承認プロセスが実行されることがあります。

    - ID 番号を追加するには、**新規** を選択します。 必要に応じてフィールドに情報を入力し、**保存** を選択します。
    - 番号を編集するには、**編集** を選択します。 必要に応じてフィールドに情報を入力し、**保存** を選択します。

7. 支払われた方法を変更するには、**自分の支払情報** タブを選択します。このタブは、**Human Resources パラメーター** ページで支払方法が有効になっている場合にのみ使用できます。 HR は、**銀行ドラフト**、**現金**、**小切手**、**電子支払**、または **その他** を有効にできます。 HR は、電子支払の検証 (米国の給与支払に使用)、および銀行口座とルート指定番号の検証を無効にすることもできます。

8. プロファイルの人事管理に表示するイメージを変更するには、**イメージ** タブを選択します。組織の設定によっては、承認のためにイメージがルーティングされる場合があります。

    - イメージをアップロードするには、**新規イメージをアップロード** を選択します。
    - イメージを削除するには、イメージを選択し、**削除** を選択します。



[!INCLUDE[footer-include](../includes/footer-banner.md)]
