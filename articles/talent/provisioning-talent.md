---
title: "Microsoft Dynamics 365 for Talent のプロビジョニング"
description: "このトピックでは、Microsoft Dynamics 365 for Talent の新しい環境のプロビジョニングについて説明します。"
author: rschloma
manager: AnnBe
ms.date: 11/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: rschloma
ms.search.scope: Talent
ms.custom: 17271
ms.assetid: ba1ad49d-8232-400e-b11f-525423506a3f
ms.search.region: Global
ms.author: rschloma
ms.search.validFrom: 2017-11-20
ms.dyn365.ops.version: Talent July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 1be4b41f63dd03a1d853d344fcde05e8962424e2
ms.openlocfilehash: e6266ef5890b5caaf33db76eeccfc8a7a6888a11
ms.contentlocale: ja-jp
ms.lasthandoff: 03/17/2018

---
# <a name="provision-microsoft-dynamics-365-for-talent"></a>Microsoft Dynamics 365 for Talent のプロビジョニング

[!include[banner](includes/banner.md)]

このトピックでは、Microsoft Dynamics 365 for Talent の新しい実稼働環境のプロビジョニングについて説明します。 このトピックでは、Talent をクラウド ソリューション プロバイダー、またはエンタープライズ アーキテクチャ (EA) 契約を通して購入したことを前提にしています。 Talent サービス プランがすでに含まれている Microsoft Dynamics 365 ライセンスがあり、このトピックの手順を完了できない場合は、サポートに問い合わせてください。

始めに、グローバル管理者は [Microsoft Dynamics Lifecycle Services](http://lcs.dynamics.com) (LCS) にサインインし、新しい Talent プロジェクトを作成します。 ライセンスの問題で Talent プロビジョニングが妨げられない限り、サポートまたは Dynamics サービス エンジニアリング チーム (DSE) の担当者に問い合わせる必要はありません

## <a name="create-an-lcs-project"></a>LCS プロジェクトの作成
Talent 環境を管理するために LCS を使用するには、最初に LCS プロジェクトを作成する必要があります。

1. Talent をサブスクライブするために使用したアカウントを使用して [LCS](https://lcs.dynamics.com/Logon/Index) にサインインします。
2. プラス記号 (**+**) を選択してプロジェクトを作成します。
3. 製品名、製品バージョンとして **Microsoft Dynamics 365 for Talent** を選択します。
4. **Dynamics 365 for Talent** の方法を選択します。
5. **作成** を選択します。

Talent を使い始める方法については、新しいプロジェクトで作成した **Talent** の方法を参照してくだい。 プロジェクトの作成が終了したら、Talent 環境を設定するために次の手順を完了してください。

## <a name="provision-a-talent-project"></a>Talent プロジェクトのプロビジョニング
LCS プロジェクトを作成した後は、環境に Talent をプロビジョニングすることができます。

1. LCS プロジェクトでは、**Talent アプリの管理** タイルを選択します。
2. Talent は PowerApps の統合および拡張機能を有効にするために Microsoft PowerApps の環境に常にプロビジョニングされています。 すでに PowerApps 環境を持っていない場合、続行する前にこのトピックの「新しい PowerApps 環境の作成 (必要な場合)」セクションにある手順に従ってください。

    > [!NOTE]
    > 既存の環境を表示、または新しい環境を作成するために、Talent をプロビジョニングするテナント管理者は PowerApps P2 ライセンスに割り当てられる必要があります。 組織に PowerApps P2 ライセンスがない場合、CSP または [PowerApps 価格ページ](https://powerapps.microsoft.com/en-us/pricing/) から入手することができます。

3. **追加**を選択し、Talent をプロビジョニングする環境を選択します。
4. 使用条件に同意、および展開を開始するために **はい** を選択します。

    新しい環境は、左のナビゲーション ウィンドウにある環境の一覧に表示されます。 ただし、配置状態が**配置済み**に更新されるまでは、環境の使用を開始できません。 このプロセスには通常、数分間かかります プロビジョニング プロセスに失敗する場合は、サポートに連絡する必要があります。

6. 新しい環境を使用するために **Talent にログオンします** を選択します。

> [!NOTE]
> 最終要件をまだサインオフしていない場合、プロジェクトに Talent のテスト インスタンスを配置することができます。 サインオフするまで、ソリューションをテストするためにこのインスタンスを使用することができます。 テストのために新しい環境を使用する場合は、実稼動環境を作成するためにこの手順を繰り返す必要があります。

> [!NOTE]
> Talent 環境は、人事管理 (HR) タスクにコンフィギュレーションされる、または Talent に指定されるデモ データを含まない LCS によってプロビジョニングされています。 デモ データを含む環境が必要な場合、60 日間無料 [Talent 試用環境](https://dynamics.microsoft.com/en-us/talent/overview/)に登録することをお勧めします。 試用環境は要求したユーザーにより所有されていますが、Core HR のシステム管理経験を通じて他のユーザーも招待できます。 試用環境には、安全にプログラムを活用するために使用する架空のデータが含まれます。 これらは実稼動環境として使用するものではありません。 試用環境が 60 日後に期限が切れると、その中にあるすべてのデータが削除され復元できないことに注意してください。 既存の環境の期限が切れた後、新しい試用環境に登録することができます。

## <a name="create-a-new-powerapps-environment-if-required"></a>新しい PowerApps 環境の作成 (必要な場合)
Talent と PowerApps 環境との統合では、PowerApps ツールを使用して Talent データの使用を統合および拡張することができます。 PowerApps 環境の目的を理解することは、Talent を拡張する必要を満たすアプリの構築に役立ちます。 環境スコープ、環境アクセス、および環境の作成および選択を含む、PowerApps 環境の詳細については、[ PowerApps 環境の発表](https://powerapps.microsoft.com/en-us/blog/powerapps-environments/) をご覧ください。 各テナントは自動的にプロビジョニングされますが、既定の PowerApps 環境が Talent の配置には最適な環境でない場合があります。 データの統合およびテスト戦略はこのステップ中に考慮する必要があります。いくつかの決定は後で変更することが容易でないため、配置に与える影響について考慮することをお勧めします。 

各テナントは既定の PowerApps 環境で自動的にプロビジョニングされますが、その環境が Talent の配置には最適な環境でない場合があります。 データの統合およびテスト戦略はこのステップ中に考慮する必要があります。 したがって、後に PowerApps 環境を変更することは容易でないため、配置へのさまざまな影響について考慮することをお勧めします。

1. LCS で、**環境の管理** を選択します。 既存の環境の表示および新しい環境の作成ができる [PowerApps 管理者センター](https://preview.admin.powerapps.com/environments) に移動します。
2. **新しい環境**を選択します。
3. 環境の一意の名前を入力し、配置する場所を選択します。

    > [!NOTE]
    > Talent はすべての地域で利用できるわけではありません。 したがって、環境の場所を選択する前に使用可能かを必ず確認してください。

4. データベースを作成するかどうかを尋ねられた場合、**データベースの作成** を選択し、Talent データの一部をホストする Common Data Service (CDS) データベースを作成します。 データベースを作成し、PowerApps アプリケーションと Talent を統合することもできます。
5. データベースに使用するアクセス レベルについて尋ねられます。 Talent ユーザーが PowerApps アプリケーションを使用して機密データに直接アクセスすることを防止するために、[**アクセスの制限**] を選択することをお勧めします。
6. 作成された CDS データベースにはデモ データが含まれます。それは他の情報の中でも、無効な従業員や架空の住所を運用環境に追加します。 デモ データを削除するには、CDS の作成が終了した後にこれらの手順に従います:

    > [!IMPORTANT]
    > 以前に CDS データベースを作成し、会社の生産データを入力した場合、これらの手順で選択したデータベース内の **すべて** のデータが (会社の実動データであっても) 削除されます。

    1. [PowerApps](https://preview.web.powerapps.com/home)に登録します。
    2. 右上のドロップダウン リストで、手順 2 で作成した環境を選択します。
    3. 左のナビゲーション ウィンドウで **Common Data Service** を展開し、**エンティティ** を選択します。
    4. ページの右側にある省略記号ボタン (**…**) を選択し、**すべてのデータをクリア** を選択します。
    5. **データを削除** を選択し、データを削除することを確認します。 このアクションは、既定で CDS に含まれているすべてのデモ データを削除します。 選択したデータベースに入力されている他のデータも削除されます。

新しい環境を使用することができるようになりました。

## <a name="grant-access-to-the-environment"></a>環境へのアクセスを付与
既定では、環境を作成したグローバル管理者がそこにアクセスできます。 ただし、追加のアプリケーション ユーザーは、明示的にアクセスを許可する必要があります。 アクセスを許可するには、Core HR 環境で [ユーザーの追加](../dev-itpro/sysadmin/tasks/create-new-users.md) および [適切なロールを割り当て](../dev-itpro/sysadmin/tasks/assign-users-security-roles.md)ます。 Attract および Onboard アプリケーションへアクセスできるよう、それらのユーザーを PowerApps 環境に追加する必要もあります。 手順をここで説明します。 手順を完了するのに助けが必要な場合は、[PowerApps 管理センターの導入](https://powerapps.microsoft.com/en-us/blog/introducing-admin-center-for-powerapps/) ブログ投稿を参照してください。

Talent 環境を展開したグローバル管理者によって、この手順が完了します。

1. [PowerApps 管理センター](https://preview.admin.powerapps.com/environments)を開きます。
2. 該当する環境をオンにします。
3. [セキュリティ] タブで、必要なユーザーを [環境メーカー] ロールに追加します。

PowerApps 環境にユーザーを手動で追加するこの最後のステップは、一時的であることに注意してください。 最終的には、ユーザーが Core HR に追加される際に、自動的に完了します。

