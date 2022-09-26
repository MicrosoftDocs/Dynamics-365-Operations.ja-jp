---
title: Lifecycle Services (LCS) のセキュリティの構成
description: この記事では、Microsoft Dynamics Lifecycle Services (LCS) のセキュリティが、組織レベルとプロジェクト レベルの両方で制御される方法について説明します。
author: AngelMarshall
ms.date: 03/15/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Developer, IT Pro
ms.reviewer: sericks
ms.custom: 6154
ms.assetid: 79396ff8-538f-4f6f-80d0-898fc5618fb5
ms.search.region: Global
ms.author: tsmarsha
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5507abba2d355f9eca7145527bc78df645770270
ms.sourcegitcommit: d3f7a56eaf788d223ece4cedac4a319eaf5f6112
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/19/2022
ms.locfileid: "9539125"
---
# <a name="configure-lifecycle-services-lcs-security"></a>Lifecycle Services (LCS) のセキュリティの構成

[!include [banner](../includes/banner.md)]
[!include [LCS deprecation](../includes/lcs-deprecation.md)]

Microsoft Dynamics Lifecycle Services (LCS) のセキュリティは、組織レベルとプロジェクト レベルの両方で制御されます。 組織のすべてのメンバーが、すべてのプロジェクトへのアクセス権を持っているわけではありません。 また、プロジェクトのメンバーは、すべて同じ組織のメンバーではない可能性があります。 <br>

現在、サイン アップ時に Microsoft 365 ポータルを作成した Microsoft Azure Active Directory (Azure AD) の資格情報を使いサイン インできます。 Azure AD の組織の管理者になっているユーザーは、Lifecycle Services (LCS) の管理者になります。 

LCS へのプロジェクト レベル アクセスは、招待によって行われます。 プロジェクトの所有者およびチーム メンバーとして組織のメンバーを招待することができます。 また、組織のメンバーではなく、Azure AD のアカンウントを持たないユーザーをチーム メンバーに招待できます。

> [!IMPORTANT]
> 会社内のすべてのユーザーを組織レベルで管理することを強くお勧めします。 また、ユーザーが組織で利用できる福利厚生にアクセスできることを確認します。

## <a name="organizational-roles"></a>組織ロール
LCS には次の 3 種類の組織ロールがあります。

- 管理者
- 寄稿者
- 代理管理者

### <a name="organization-admin"></a>組織の管理者
組織またはテナント レベルでは、LCS にサイン インすると、Azure AD のグローバル管理者ロールを持つすべてのユーザーは自動的に組織管理者になります。 その後、管理者は現在管理者に貢献している他のユーザーを昇格できます。 管理者には固有の機能があります。 たとえば、以前にプロジェクトに参加していなくても、テナントが所有する任意のプロジェクトにプロジェクトの所有者として自分自身を追加できます。

![組織管理者はすべてのプロジェクトに自身を追加できると言う LCS のメッセージ。](media/OrgAdminProjectInject.png "組織管理者はすべてのプロジェクトに自身を追加できると言う LCS のメッセージ")

さらに、管理者は[複数の LCS プロジェクトを作成](../../fin-ops/get-started/implement-multiple-projects-aad-tenant.md#create-multiple-lcs-projects) の手順に従い、追加の LCS 実装プロジェクトを作成できます。

### <a name="organization-contributor"></a>組織の共同作成者
共同作成者は Azure AD テナントからの他のユーザーですが、管理者機能を持たないユーザーです。 共同作成者はプロジェクトを作成できます。 また、サインインするテナントの最初のユーザーであり、該当する財務と運用アプリのライセンスを購入した後、最初の実装プロジェクトを作成することもできます。

### <a name="delegated-admin"></a>代理管理者
ユーザーが Microsoft パートナー テナントからで、顧客組織と確立された関係を持つ場合を除いて、委任された管理者ロールは管理者ロールと同じです。 委任された管理者は顧客の代わりにサイン インし、必要な操作を実行して必要なサポートを提供できます。

## <a name="manage-lcs-organization-users"></a>LCS 組織のユーザーの管理
管理者のみユーザーを管理できます。 以下の手順を実行します。

1.  PartnerSource ビジネス センター (PSBC)、または Azure AD で、LCS へのアクセスを必要とする組織内のすべてのユーザーを組織と関連付けます。 ユーザーは、LCS にログインできるようになるまでに、2 営業日待機することが必要な場合があります。
2.  LCS の適切なプロジェクトに、ユーザーを追加します。

### <a name="invite-a-user-to-an-lcs-project"></a>LCS プロジェクトへのユーザーの招待

1.  [LCS](https://lcs.dynamics.com/) にサインインします。
2.  プロジェクトを選択してユーザーを追加します。
3.  **プロジェクト ユーザー** タイルを選択し、**プロジェクト ユーザー** ページで、プラス記号 (**+**) を選択します。
4.  ユーザーの電子メール アドレスを入力し、次に正しいセキュリティ ロールを選択して、**招待** を選択します。

> [!NOTE]
> 実装プロジェクトで、招待されたユーザーの実装ロールを選択できます。 **FastTrack からの連絡を許可する** を **はい** に設定した場合、Microsoft FastTrack チームは実装ロールと実装プロジェクトのステージに基づいてご連絡を差し上げる場合があります。   


## <a name="configuring-project-security"></a>プロジェクト セキュリティのコンフィギュレーション
プロジェクトにユーザーとして参加するように、組織の内外からユーザーを招待することができます。 次のテーブルに、ユーザーが使用可能なロールを示します。

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>役割</th>
<th>説明</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>プロジェクト所有者</td>
<td>このロールのメンバーは LCS のすべてのツールにアクセスでき、他のユーザーを任意のロールに追加することや、プロジェクトを削除することができます。</td>
</tr>
<tr class="even">
<td>環境マネージャー</td>
<td>このロールのメンバーは LCS のすべてのツールにアクセスでき、クラウド ホスト環境を管理できます。</td>
</tr>
<tr class="odd">
<td>プロジェクト チーム メンバー</td>
<td>このロールのメンバーは LCS のすべてのツールにアクセスできますが、クラウド ホスト環境を管理できません。</td>
</tr>
<tr class="even">
<td>プロジェクト チーム メンバー (見込顧客)</td>
<td>このロールのメンバーは LCS プロジェクトのすべてのツールに制限付きでアクセスできます。 見込顧客は、プロジェクトに追加されましたが、VOICE または Azure AD にアカウントを持っていないユーザーです。 <strong>見込み顧客</strong>が組織として一覧表示されるため、ユーザーが見込み顧客であることを識別することができます。</td>
</tr>
<tr class="odd">
<td>Operations user</td>
<td>このロールのメンバーは LCS の次のツールにアクセスできます。
<ul>
<li>システム診断</li>
<li>問題検索</li>
<li>クラウドを利用したサポート</li>
<li>更新</li>
<li>クラウド ホスト環境</li>
</ul></td>
</tr>
</tbody>
</table>

1 つのプロジェクトのセキュリティをコンフィギュレーションした後は、別のプロジェクトにユーザーをインポートできます。

## <a name="configure-implementation-roles"></a>実装ロールのコンフィギュレーション 
実装プロジェクトがある場合、プロジェクト ユーザーの実装ロールを指定するためのオプションが表示されます。 詳細については、[Dynamics 365 実装のロール](/training/modules/get-started-implementation-project/01-2-roles) を参照してください。


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
