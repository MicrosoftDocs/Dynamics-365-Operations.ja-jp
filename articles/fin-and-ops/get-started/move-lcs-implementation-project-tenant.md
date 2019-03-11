---
title: LCS 実装プロジェクトを別の Azure AD テナントに移動する
description: このトピックでは、サブスクリプションと LCS 実装プロジェクトを異なる Azure AD テナントに移動する方法について説明します。
author: ClaudiaBetz-Haubold
manager: AnnBe
ms.date: 06/08/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: IT Pro
ms.reviewer: kfend
ms.search.scope: Operations
ms.search.region: Global
ms.author: chaubold
ms.search.validFrom: 2018-05-30
ms.dyn365.ops.version: AX 7.0
ms.openlocfilehash: 8663d0eaebe8cae33256220e96feebb3baac259e
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/29/2019
ms.locfileid: "369048"
---
# <a name="move-lcs-implementation-projects-to-different-azure-ad-tenants"></a>LCS 実装プロジェクトを別の Azure AD テナントに移動する

[!include [banner](../includes/banner.md)]

サブスクリプションと Microsoft Dynamics Lifecyle Services (LCS) 導入プロジェクトを別の Microsoft Azure Active Directory (Azure AD) テナントに移すことができます。 この移動が必要になる場合のいくつかのシナリオを次に示します。

- 誤ってサブスクリプションが正しくない Azure AD テナントに対して購入されました。

    > [!NOTE]
    > クラウド サービス プロバイダーであり、既存の顧客に Microsoft Dynamics 365 for Finance and Operations のサブスクリプションを販売する場合は、その顧客との再販業者関係を要求して、顧客の既存の Azure AD テナントにサブスクリプションを配置する必要があります。 Microsoft パートナー センターで新しい顧客レコードを作成する場合、顧客の新しい Azure AD テナントを作成します。

- サブスクリプションが購入された後、顧客は Azure AD テナントの構造を変更します。

定期購読および関連するすべてのコンポーネントの移動のプロセスには、次の図に示すように、次の 4 つの主要なステップがあります。

![定期売買を移動するためのプロセス](./media/move-subscription-process.png)

## <a name="activate-subscriptions-on-the-new-tenant"></a>新しいテナントのサブスクリプションを有効化

クラウド サービス プロバイダまたはボリューム ライセンスの再販業者と協力して、新しい Azure AD テナントに対するサブスクリプションを有効にします。 ユーザーおよびアドオン環境のすべてのサブスクリプションを有効にする必要があります。

### <a name="cloud-service-provider"></a>クラウド サービス プロバイダー

Microsoft クラウド ソリューション プロバイダー (CSP) 契約を通じてライセンスを取得している場合は、クラウド サービス プロバイダーから新しいテナントに対して必要なサブスクリプションを購入してください。 新しいテナントが既に存在する場合、クラウド サービス プロバイダは、再販業者関係を要求する必要があります。 または、パートナー センターのクラウド サービス プロバイダで必要な既定ドメイン名の新しい顧客を作成する必要があります**\*.onmicrosoft.com** (たとえば、**contoso.onmicrosoft.com**)。

クラウド サービス プロバイダーに、今回は既存のサブスクリプションを中断しないよう依頼します。

### <a name="volume-licensing"></a>ボリューム ライセンス

Microsoft ボリューム ライセンス契約を通じてライセンスを取得している場合は、[ボリューム ライセンス サポート センター](https://www.microsoft.com/Licensing/servicecenter/Help/Contact.aspx)に連絡し、サブスクリプションを古いテナントから新しいテナントに再マップするように依頼する必要があります。 Microsoft Office 365 管理センターからボリューム ライセンスのサポートに連絡することができます。 定期売買が両方のテナントで有効になると、支払猶予期間を要求します。 顧客プライバシーの問題が原因で、顧客がこの要求を実行する必要があります。 次の情報が必要です。

- 公的顧客番号
- 登録番号
- 現在プロビジョニングされている定期売買の現在のテナント ドメイン
- 顧客が定期売買のプロビジョニングを希望する宛先テナント ドメイン
- 顧客が違うテナントに移行したボリューム ライセンス サブスクリプションを必要とする理由の詳細説明
- 新しいテナントに移動しなければならない有料サブスクリプションの総数、サブスクリプション タイプおよび定員数

> [!IMPORTANT]
> 古いテナントで LCS の廃棄が完了するまでの数週間、定期売買が両方のテナントで並行して有効であることが非常に重要です。

## <a name="configure-lcs-on-the-new-tenant"></a>新しいテナントに LCS をコンフィギュレーションします。

新しいテナントで、開始し設定する必要がある新しい LCS プロジェクトを取得します。

1. LCS を完全に構成します。 コンフィギュレーションの一部として、ユーザー、Microsoft Azure DevOps アソシエーション、サブスクリプション見積り、アセット ライブラリおよびビジネス プロセス モデラー (BPM) などを追加する必要があります。
2. 新しい LCS プロジェクトのすべての非運用環境を配置します。
3. 必要なコード パッケージを環境に適用します。
4. 環境にデータをアップロードします。 データ パッケージを使用してデータを移動することも、データベースを復元することもできます。 データベースを復元する場合は、いくつかのプロパティを新しいテナントに再マップするために追加の手順が必要です。
5. ユーザー情報を更新します。

    1. 管理者ユーザーを除くすべてのユーザー アカウントを削除します。
    2. USERINFO の管理者ユーザー レコードを修正します。

        ```
        UPDATE USERINFO
        SET SID='mysid', NETWORKALIAS='myalias/email', NETWORKDOMAIN='https://sts.windows.net'
        WHERE ID = 'Admin'
        ```

6. 正しいセキュリティ識別子 (SID) および ID プロバイダーを持つ他のすべてのユーザーを再インポートします。
7. 適切なテーブルでテナント ID を更新するには、次のコマンドを実行します。

    - 名前 = 'TENANTID' の際は SYSSERVICECONFIGURATIONSETTING から VALUE を選択します
    - POWERBICONFIG から TENANTID を選択します
    - PROVISIONINGMESSAGETABLE から TENANTID を選択します
    - B2BINVITATIONCONFIG から TENANTID を選択します
    - RETAILSHAREDPARAMETERS から TENANTID を選択します

8. 環境を完全に構成します。 この手順の一部として、統合のエンドポイントをコンフィギュレーションします。
9. 新しい LCS プロジェクトのユーザー受け入れテスト (UAT) 環境でスモーク テストを実行します。 これらのテストでは、ユーザーのサインイン、統合、ワークフロー、印刷、レポート、および構成やユーザー情報に依存する同様のプロセスに焦点を当てる必要があります。
10. 実稼働環境を既に配置している場合は、すべてのサンドボックス環境の移動が終了し、UAT を完了した後に、新しいテナントに移動するためのサポート要求を開く必要があります。 実稼働環境を新しいテナントに移動するプロセスには、48 ～ 72 時間のダウンタイムの延長が必要です。

ソリューションとスコープに応じて、新しい Azure AD テナントで追加の手順を実行する必要があります。 これらの手順には、アプリケーションの登録 (定期的な統合と倉庫管理のため)、ドメインの追加、およびシングル サインオン (SSO) を有効にするディレクトリ同期の設定が含まれます。

Web サービスへの呼び出しが、環境の**ホーム**テナントからのみ許可されていることに注意してください。 たとえば、元のテナントは companya.com であり、統合は `services@companya.com` として実行されました。 この場合、テナントを companyb.com に切り替えると、**userInfo.networkdomain** を `https://sts.windows.net/companyb.com` に更新してもWeb サービスの呼び出しに対して `services@companya.com` を使用できなくなります。

> [!IMPORTANT]
> この期間中、2 つの並列 LCS プロジェクトがあります。 LCS 内の**利用可能なサブスクリプション**ページの LCS プロジェクトに関連付けられている Azure AD テナントの名前と ID を確認できます。 Azure Blob Storage に保存されている添付ファイルを処理するドキュメントは失われます。

## <a name="delete-environments-on-the-old-tenant"></a>古いテナントの環境の削除

新しい Azure AD テナントに対する新しい LCS プロジェクトが完全に機能した後、古い LCS プロジェクトで環境を停止、開放および削除する必要があります。 完了したとき、**コンフィグレーション** ボタンは環境ごとに使用できるようになります。 後で必要になる可能性のある残りのコンポーネントは、アセット ライブラリから保管する必要があります。 Microsoft は、顧客のアカウントを無効にし、サービスが長期間にわたって中断された後に顧客データを削除する権限を保有します。

## <a name="suspend-subscriptions-on-the-old-tenant"></a>古いテナントで定期売買を中断します。

1. すべての環境が削除されると、必要な LCS コンポーネントを保存し、クラウド サービス プロバイダまたは Volume Licensing Support と協力して、以前の Azure AD テナントのすべてのライセンスを中断します。

    - **クラウド サービス プロバイダー:** 古いテナントに対して既存の定期売買を中断します。
    - **ボリューム ライセンス サポート:** 作業が完了したこと、およびサブスクリプションが古いテナントに対してすぐ中断することを確認するボリューム ライセンス サポート センター。

2. 古い LCS プロジェクトを削除するサポート チケットをファイルします。
