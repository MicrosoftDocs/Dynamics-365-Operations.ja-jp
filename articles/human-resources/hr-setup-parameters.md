---
title: Human Resources パラメーターのコンフィギュレーション
description: このトピックでは、Dynamics 365 Human Resources で会社固有のパラメーターを設定する方法を説明します。
author: andreabichsel
ms.date: 06/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: HRMParameters, HcmPersonnelManagementWorkspace
audience: Application User
ms.search.scope: Human Resources
ms.custom: 51941
ms.assetid: 2cfb061a-a616-4bf9-9d98-9cde00039eec
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 24d30aa06805b530cc069be0517279a11dff9ed4
ms.sourcegitcommit: c08a9d19eed1df03f32442ddb65a2adf1473d3b6
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/06/2021
ms.locfileid: "6356539"
---
# <a name="configure-human-resources-parameters"></a>Human Resources パラメーターのコンフィギュレーション

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

他のパラメーター設定は会社固有ですが、人事管理のパラメーター設定は会社間で共有されます。 このトピックでは、会社固有の人事管理のパラメーターを設定する方法を説明します。

2 つのページが人事管理のパラメータの設定に使用されます。 会社間で共有されるパラメータに、**人事管理の共有パラメーター** ページを使用します。 会社固有のパラメータ (つまり、設定を単一の会社に適用する場合) に、**人事管理パラメータ** ページを使用します。

![人事管理パラメーターに移動する。](./media/hr-employee-self-service-human-resources-parameters.png)

**人事管理パラメーター** ページで、設定は 6 つのタブに分割されます:

- **全般**
- **採用** (これは Dynamics 365 Human Resources には含まれていません)
- **報酬**
- **番号順序**
- **FMLA**
- **従業員セルフ サービス**
- **マネージャー セルフ サービス**
- **給付金管理**
- **休暇**
- **支払方法**

各タブには単一の会社に関する情報が含まれます。

## <a name="general"></a>全般

**概要** タブの設定は、休暇、傷害と疾病、新規採用に関する情報の外観を定義します。 このタブの設定は、作業中と表示される既定のエントリも定義します。 特に、このタブでは次のことができます。

- 未処理の休暇トランザクションに適用する色を選択します。
- レポートに使用するスタイル シートを指定します。
- トレーニング コースと休暇登録間の統合を有効にします。
- この統合を制御するために使用する休暇コードを選択します。
- けが/病気のケース インシデントを保持する期間を示します。
- 新しい従業員の雇用時に表示される既定の ID 番号を指定します。
- 勤続年数の計算に使用する日付を指定します。 

![一般タブ。](./media/hr-setup-parameters-general.png)

## <a name="recruitment"></a>採用

**採用** タブの設定では、申請者に自動的に送信される通信文書に使用するドキュメント タイプを定義します。 未承諾の申請に使用される採用プロジェクトを示すこともできます。

採用プロジェクトのエイジングとして定義されている期間によって、**採用管理** ワークスペースの、**エイジング プロジェクト** タイルに含まれている採用プロジェクトが決まります。 **採用** ワークスペースの、**申請の期限が近づいています** タイルで申込期限が近づいている採用プロジェクトを表示するために、申請の期限の警告に定義されている期間が使用されます。

採用の詳細については、[職務候補者の採用](hr-personnel-recruit.md)を参照してください。

## <a name="compensation"></a>報酬

Dynamics 365 Finance では、**報酬** タブの設定は、ユーザーが固定または変動報酬プランの情報を保存するかどうかの確認を定義します。 **保存の検証を有効にします** をオンにすると、そのユーザーが報酬に関連付けられたページを閉じるときに、レコードを保存するかどうか確認するメッセージが表示されます。 報酬管理の一部のページでは、ユーザーが情報を削除することはできません。 ユーザーに情報を保存するかどうかを確認するよう促すことにより、後で削除できない保存される情報の量を限定できる場合があります。 **保存の検証を有効にします** をオフにすると、場合によってはユーザーの準備が整う前に、レコードはすぐに保存されます。 パフォーマンス管理を使用している場合は、**報酬** タブでも、パフォーマンスを評価するときに報酬プランに割り当てられているモデルの代わりに使用する評価モデルを選択できます。

人事管理では、**報酬** タブを使用して、報酬プランへのアクセスの制限や、既定の通貨の設定を選択できます。

報酬の詳細については、[報酬プランの概要](hr-compensation-overview.md)を参照してください。

![報酬タブ。](./media/hr-setup-parameters-compensation.png)

## <a name="number-sequences"></a>番号順序

**番号順序** タブの設定により、次のような人事管理の品目に対して自動的に ID を割り当てるために使用する順序が決定されます。

- アプリケーション
- 休暇登録
- 報酬プロセスの結果
- ケース番号
- コース
- コースの議題

番号順序およびコードを管理するには、**番号順序** リスト ページを使用します (**組織管理 > 番号順序 > 番号順序** の順に選択します)。

詳細については、[番号順序の概要](../fin-ops-core/fin-ops/organization-administration/number-sequence-overview.md?toc=%2fdynamics365%2fhuman-resources%2ftoc.json)を参照してください。

> [!NOTE]
> 作業時間数は 1,250 を超えることはできず、雇用期間は 12 か月を超えることはできません。 これらの最大値は米国の連邦法に従います。

![番号順序タブ。](./media/hr-setup-parameters-number-sequences.png)

## <a name="fmla"></a>FMLA

FMLA タブでは、FMLA 資格条件と、FMLA 資格付与時間を設定します。 詳細については、[休暇および欠勤パラメーターのコンフィギュレーション](hr-leave-and-absence-parameters.md) を参照してください。

![FMLA タブ。](./media/hr-setup-parameters-fmla.png)

## <a name="employee-self-service"></a>従業員セルフ サービス

**従業員セルフ サービス** タブの設定は、従業員セルフ サービスが従業員にどのように表示されるかに影響します。 このタブで次の操作を実行できます。

- 従業員セルフサービス ワークスペースの名前を入力します
- 従業員に対してマネージャが入力できる情報を選択します
- 従業員向けに役立つリンクを追加します
- 従業員がビジネスの連絡先情報を追加または編集するのを制限します。 詳細については、[個人情報の編集の制限](hr-employee-self-service-restrict-editing.md)を参照してください。

従業員セルフ サービスの設定の詳細については、[従業員およびマネージャー セルフ サービスの概要](hr-employee-manager-self-service-overview.md)を参照してください。

![従業員セルフ サービス タブ。](./media/hr-setup-parameters-employee-self-service.png)

## <a name="manager-self-service"></a>マネージャー セルフ サービス

**マネージャー セルフ サービス** の設定は、マネージャーがマネージャー セルフ サービスに表示する内容に影響します。 このタブでは、次のオプションを構成できます。

- 期限が切れるレコードの範囲
- マネージャーが期限が切れるレコードで表示できる情報
- マネージャーが拡張レポートの空いている職位を表示できるかどうか
- 既存の作業者の表示
- マネージャー向けに役立つリンク

マネージャー セルフ サービスの設定の詳細については、[従業員およびマネージャー セルフ サービスの概要](hr-employee-manager-self-service-overview.md)を参照してください。

![マネージャー セルフ サービス タブ。](./media/hr-setup-parameters-manager-self-service.png)

## <a name="benefits-management"></a>給付金管理

給付金管理タブで、給付金管理の電子メール オプションを構成できます。 給付金管理の設定および使用の詳細については、[給付金管理の概要](hr-benefits-management-overview.md)を参照してください。

![給付金管理タブ。](./media/hr-setup-parameters-benefits-management.png)

## <a name="leave-and-absence"></a>休暇

休暇と欠勤の設定および使用の詳細については、[休暇と欠勤の概要](hr-leave-and-absence-overview.md)を参照してください。

## <a name="payment-methods"></a>支払方法

**支払方法** タブで、組織でサポートされている支払方法を選択できます。 報酬の構成の詳細については、[報酬プランの概要](hr-compensation-overview.md)を参照してください。

![支払方法タブ。](./media/hr-setup-parameters-payment-methods.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
