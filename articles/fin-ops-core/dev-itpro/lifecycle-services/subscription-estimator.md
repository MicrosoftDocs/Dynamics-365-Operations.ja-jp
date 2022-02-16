---
title: Lifecycle Services (LCS) のサブスクリプション試算
description: このトピックでは、Lifecycle Services (LCS) で利用可能なサブスクリプション試算ツールを使用する方法について説明します。
author: angelmarshall
ms.date: 01/25/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Developer, IT Pro
ms.reviewer: sericks
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: tsmarsha
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: Platform update 12
ms.openlocfilehash: cbabd7d496d6285eaef9704842038856c7a94cab
ms.sourcegitcommit: 1a00bebfb2cee8274331f3bbbd890e1a99bbab8e
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/26/2022
ms.locfileid: "8028466"
---
# <a name="subscription-estimator-in-lifecycle-services-lcs"></a>Lifecycle Services (LCS) のサブスクリプション試算

[!include [banner](../includes/banner.md)]

サブスクリプション見積もりツールは、Microsoft Dynamics Lifecycle Services (LCS) で使用できるツールです。 Microsoft は、このツールを使用して、顧客に対して準備する必要がある実稼働環境の初期サイズを見積ります。 顧客が実稼働環境の配置を要求する前に、トランザクション カウントの観点からピーク作業負荷を見積もり、その情報を LCS にアップロードする必要があります。 ユーザー ライセンスの詳細およびトランザクション カウントを使用してサブスクリプション要件を推測することにより、サブスクリプション見積もりツールは、プロビジョニングされた環境が顧客の業務要件を満たしていることを確認できます。

サブスクリプション試算ツールを使用するには、これらの手順に従います。

1. LCS で、実装プロジェクトに関連付けられているプロジェクトを開きます。
2. ページの上部にあるハンバーガー アイコン選択し、**サブスクリプション見積もりツール** を選択します。

    [![サブスクリプション見積もりツール。](./media/subscription_estimator_01.png)](./media/subscription_estimator_01.png)

3. サンプルの使用状況プロファイルをダウンロードします。
4. 各タブで必要な質問に回答します。Commerce の顧客の場合は、**Retail と Commerce** タブ上の質問に回答してください。
5. 使用状況プロファイルをローカルに保存します。
6. 使用プロファイルをアップロードするには、**新しい見積もり** を選択し、見積もりに名前を付け、使用プロファイルをアップロードします。
7. アップロードが完了した後、**アクティブとしてマークする** を選択し見積もりを有効にします。 生産の配置をコンフィギュレーションするために有効な見積が必要です。

有効でアクティブな見積があるときは、**構成** ボタンが使用できるようになります。 このボタンを使用すると、製造環境の展開を要求することができます。

## <a name="edit-the-estimate-for-multiple-implementation-projects"></a>複数の実装プロジェクトの見積を編集する

複数の実装プロジェクトの見積を編集するためには、次の手順を実行します。

1. 各実装プロジェクトのサブスクリプション見積ツールを開いてください。
2. 有効なサブスクリプション見積を編集して、各プロジェクトにライセンス配賦を適用します。 サブスクリプション見積ツールでサブスクリプション見積を編集するには、見積を選択してから **見積を編集** ボタンを選択します。

    [![サブスクリプション見積ツールで有効なサブスクリプション見積。](./media/SubscriptionEstimatorWithEdit.jpg)](./media/SubscriptionEstimatorWithEdit.jpg)

3. **見積を編集** ダイアログ ボックスで、Finance and Operations ライセンスの各タイプのライセンス カウントを入力します。 既定では、各サブスクリプション見積が作成された際、購入した全てのライセンスの全カウントは割り当てられます。 顧客は、ライセンスの総数を超えるライセンスを 1 つの見積に割り当てることはできません。 また、割り当てられた番号を Dynamics 365 ライセンス ポリシーで必要な最小数よりも小さい値に減らす必要があります。

    [![サブスクリプション見積ツールで有効なダイアログ ボックスを編集。](./media/SubscriptionEstimatorEditDialog.jpg)](./media/SubscriptionEstimatorEditDialog.jpg)

4. **保存** を選択します。
5. 有効な見積に対する更新を行った場合、実稼働環境のサイズが変更される場合があるという警告が表示されます。 **はい** を選択して、更新を続行することを確認します。

    [![サブスクリプション見積ツールの有効な見積の更新に関する警告メッセージ。](./media/SubscriptionEstimatorEditDialogWarning.jpg)](./media/SubscriptionEstimatorEditDialogWarning.jpg)

> [!NOTE]
> 複数の見積を使用できますが、1 つの見積に **アクティブ** とマークする必要があります。 実稼動環境が配置された後、または環境の配置がサインオフされた後、有効な見積はロックされます。 有効な見積を追加変更したり、新しい見積を **有効** としてマークすると、実稼働環境のサイズが変更される場合があります。

## <a name="frequently-asked-questions"></a>よく寄せられる質問

### <a name="why-isnt-the-configure-button-for-deploying-a-production-environment-available-even-though-there-is-an-active-estimate-and-why-does-a-warning-message-appear-in-the-action-center-on-the-project-dashboard"></a>アクティブな見積があるにもかかわらず、実稼動環境のコンフィギュレーション ボタンが有効なのはなぜですか? また、プロジェクト ダッシュ ボード上のアクション センターに警告メッセージが表示されるのはなぜでしょうか?

複数の実装プロジェクトがある場合、**コンフィギュレーション** ボタンを有効にされていない可能性があり、アクション センターに不足しているライセンス数に関する警告メッセージが表示されます。 サブスクリプション見積ツールの **見積を編集** ボタンで、有効なサブスクリプション見積を編集およびそのプロジェクトに必要なライセンス配分を適用することができます。

### <a name="why-does-an-error-occur-when-i-mark-an-estimate-as-active"></a>見積に有効とマークするとエラーが発生するのはなぜですか?

見積を **有効** とマークすると、次のエラー メッセージが表示されることがあります。

*見積が作成されましたが、要件を満たしていません*

このエラーは、入力されたトランザクション明細行がサブスクリプション見積ツールの制限内にない場合に発生します。 このエラーを解決するには、サポート要求を作成し、使用プロファイルを添付します。 次に、インスタンスのサイズを手動で変更できます。

### <a name="how-can-i-update-my-subscription-if-my-production-environment-is-deployed"></a>実稼動環境が配置されている場合、どのようにサブスクリプションを更新ことができますか?

[サブスクリプション見積](subscription-estimator.md) は、プロダクションを要求をする前に必要なステップです。 複数の見積を使用できますが、1 つの見積に **アクティブ** とマークする必要があります。 有効なサブスクリプション見積を使用して、実稼働環境のサイズを変更することができます。 実稼動環境が配置された後、または環境の配置がサインオフされた後、有効な見積はロックされます。 有効なサブスクリプション見積を編集するには、サブスクリプション見積ツールの **見積を編集** ボタンを選び、ライセンス配分を更新します。

### <a name="what-should-i-do-to-activate-my-subscription-estimate-if-i-have-multiple-projects-in-the-same-tenant"></a>同じテナントに複数のプロジェクトがある場合、サブスクリプション見積を有効にするには何をする必要がありますか?

同じテナント内に複数のプロジェクトを実装する場合、LCS のアクション センターに「サブスクリプション見積が完了していない」ことを示す警告が表示されることがあります。 こ警告は、すべての実装プロジェクトの見積ユーザーの数が、購入したライセンスの数を超えないようにする必要があることを示しています。 この状況は、有効なサブスクリプション見積のユーザー合計が、同じタイプのテナント ライセンス数を上回っている場合に発生することがあります。 有効なサブスクリプション見積を編集するには、サブスクリプション見積ツールの **見積を編集** ボタンを選び、ライセンス配分を更新します。

> [!NOTE]
> FastTrack ソリューション アーキテクトは、サブスクリプション見積のアップロードまたは更新には関与していません。 LCS のサブスクリプション見積に関する警告が特定された場合、このトピックの指示に従ってください。 問題が継続する場合、Microsoft サポートに問い合わせてください。

その他のエラー メッセージが表示されたり、他の問題が発生した場合は、サポート チームがその問題に対処できるように、サポート リクエストを作成し、有効な見積を添付します。

## <a name="additional-resources"></a>追加リソース

[サブスクリプション、LCS プロジェクト、および Azure Active Directory テナントに関するよく寄せられる質問](../../fin-ops/get-started/subscription-overview.md)

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
