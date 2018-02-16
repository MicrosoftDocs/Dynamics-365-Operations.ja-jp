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
ms.sourcegitcommit: a53c1997f74ebe572b17cc3090d2e236b6fe78f6
ms.openlocfilehash: 8a84cfe9b73f0c72f3cb0c3843749754c6b3d538
ms.contentlocale: ja-jp
ms.lasthandoff: 01/31/2018

---
# <a name="provision-microsoft-dynamics-365-for-talent"></a>Microsoft Dynamics 365 for Talent のプロビジョニング
このトピックでは、Microsoft Dynamics 365 for Talent の新しい環境のプロビジョニングについて説明します。 このトピックでは、Talent をクラウド ソリューション プロバイダー、またはエンタープライズ アーキテクチャ (EA) 契約を通して購入したことを前提にしています。 Talent サービス プランがすでに含まれている Microsoft Dynamics 365 ライセンスがあり、このトピックの手順を完了できない場合は、サポートに問い合わせてください。

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

    新しい環境は、左のナビゲーション ウィンドウにある環境の一覧に表示されます。 ただし、配置状態が**配置済み**に更新されるまでは、環境の使用を開始できません。 このプロセスには通常、数分間かかります プロビジョニングに失敗する場合、サポートに連絡する必要があります。

6. 新しい環境を使用するために **Talent にログオンします** を選択します。

> [!NOTE]
> 最終要件をまだサインオフしていない場合、プロジェクトに Talent のテスト インスタンスを配置することができます。 サインオフするまで、ソリューションをテストするためにこのインスタンスを使用することができます。 テストのために新しい環境を使用する場合は、実稼動環境を作成するためにこの手順を繰り返す必要があります。

## <a name="create-a-new-powerapps-environment-if-required"></a>新しい PowerApps 環境の作成 (必要な場合)

Talent の PowerApps 環境との統合の背後にあるビジョンは、Talent データ上に PowerApps ツールを使用してデータの統合と拡張を可能にすることです。 結果として、Talent に使用する環境を選択するとき、PowerApps 環境の目的を理解することが大切になります。 環境スコープ、環境アクセス、および環境の作成および選択を含む、PowerApps 環境の詳細については、[ PowerApps 環境の発表](https://powerapps.microsoft.com/en-us/blog/powerapps-environments/) をご覧ください。  各テナントは既定の PowerApps 環境で自動的にプロビジョニングされますが、Talent の配置には最適な環境でない場合があります。 データの統合およびテスト戦略はこのステップ中に考慮する必要があります。後で変更することは容易ではないため、環境へのさまざまな影響について考慮することをお勧めします。

1. LCS の **環境の管理]** を選択します。 既存の環境の表示および新しい環境の作成ができる [PowerApps 管理者センター](https://preview.admin.powerapps.com/environments) に移動します。
2. (**+**) **新しい環境** ボタンを選択します。
3. 環境の一意の名前を入力し、配置する場所を選択します。

    > [!NOTE]
    > Talent はすべての地域で利用できるわけではありません。 したがって、環境の場所を選択する前に使用可能かを必ず確認してください。

4. データベースを作成するかどうかを尋ねられた場合、**データベースの作成** を選択し、Talent データの一部をホストする Common Data Service (CDS) データベースを作成します。 データベースを作成し、PowerApps アプリケーションと Talent を統合することもできます。
5. データベースに使用するアクセス レベルについて尋ねられます。 Talent ユーザーが PowerApps アプリケーションを使用して機密データに直接アクセスすることを防止するために、[**アクセスの制限**] を選択することをお勧めします。
6. 作成される CDS データベースにはデモ データが含まれます。 このデモ データは、デモ データの会社を使用してテストを行う、またはタスク記録およびタスク ガイドを作成する際に役立ちます。 ただし、デモ データは、他の情報の中でも、無効な従業員や架空の住所を運用環境に追加します。 デモ データを削除するには、CDS の作成が終了した後にこれらの手順に従います:

    > [!IMPORTANT]
    > 以前に CDS データベースを作成し、会社の生産データを入力した場合、これらの手順で選択したデータベース内の **すべて** のデータが (会社の実動データであっても) 削除されることに注意してください。

    1. [PowerApps](https://preview.web.powerapps.com/home) へのサインイン、およびページの右側にあるドロップダウンのステップ 2 で作成した環境を選択します。
    2. 左のナビゲーション ウィンドウで [**Common Data Service**] を展開し、[**エンティティ**] を選択します。
    3. ページの右側にある省略記号ボタン (**…**) を選択し、**すべてのデータをクリア** を選択します。
    4. **データを削除** を選択し、データを削除することを確認します。 このアクションは、既定で CDS に含まれているすべてのデモ データを削除します。 選択したデータベースに入力されている他のデータも削除されます。
    
新しい環境を使用することができるようになりました。

## <a name="granting-access-to-the-environment"></a>環境へのアクセスを付与
既定では、環境を作成したグローバル管理者がアクセスすることが可能ですが、追加のアプリケーション ユーザーはアクセスを明示的に許可される必要があります。 これは Core HR 環境内の [ユーザーを追加](../dev-itpro/sysadmin/tasks/create-new-users.md) および [適切なロールへの割り当て](../dev-itpro/sysadmin/tasks/assign-users-security-roles.md) により行うことができます。 また、Attract および Onboard アプリケーションへアクセスするために、それらのユーザーを PowerApps 環境に追加する必要もあります。  ブログ記事 [PowerApps 管理センターの導入](https://powerapps.microsoft.com/en-us/blog/introducing-admin-center-for-powerapps/) はここに説明されたこれらステップを完了するために役立ちます。

> 1.    Talent 環境を配導入したグローバル管理者は [PowerApps 管理者センター](https://preview.admin.powerapps.com/environments) に移動する必要があります。   
> 2.    対象の環境を選択します。
> 3.    [セキュリティ] タブで、必要なユーザーを [環境メーカー] ロールに追加します。

PowerApps 環境にユーザーを追加するこの最後のステップは、一時的であることに注意してください。 最終的に、Core HR 内でユーザーが追加されたときにこれを自動的に有効にする機能が追加されます。


