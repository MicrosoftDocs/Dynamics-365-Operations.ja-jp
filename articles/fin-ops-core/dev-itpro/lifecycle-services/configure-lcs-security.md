---
title: Lifecycle Services (LCS) のセキュリティの構成
description: このトピックでは、Microsoft Dynamics Lifecycle Services (LCS) のセキュリティが、組織レベルとプロジェクト レベルの両方で制御される方法について説明します。
author: AngelMarshall
manager: AnnBe
ms.date: 12/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Developer, IT Pro
ms.reviewer: sericks
ms.custom: 6154
ms.assetid: 79396ff8-538f-4f6f-80d0-898fc5618fb5
ms.search.region: Global
ms.author: tsmarsha
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 73c2fd242cbb9057b4a6f711b50d7cb9049b5fb3
ms.sourcegitcommit: 79621e667cd7f48ba3bdbf2731f6f33d8e9f57f6
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/10/2021
ms.locfileid: "5154319"
---
# <a name="configure-lifecycle-services-lcs-security"></a>Lifecycle Services (LCS) のセキュリティの構成

[!include [banner](../includes/banner.md)]

Microsoft Dynamics Lifecycle Services (LCS) のセキュリティは、組織レベルとプロジェクト レベルの両方で制御されます。 組織のすべてのメンバーが、すべてのプロジェクトへのアクセス権を持っているわけではありません。 また、プロジェクトのメンバーは、すべて同じ組織のメンバーではない可能性があります。 <br>

現在、サインアップ時に [Microsoft 365 ポータル](https://go.microsoft.com/fwlink/?LinkID=324287)で作成した Microsoft Azure Active Directory (Azure AD) 資格情報を使用してサインインすることができます。 Azure AD の組織の管理者になっているユーザーは、Lifecycle Services (LCS) の管理者になります。 <br> 

Microsoft Dynamics AX 2012 では、LCS への組織レベルのアクセスは、個人の Microsoft ID と CustomerSource または PartnerSource の組織との関連付けによって制御されます。 したがって、CustomerSource または PartnerSource のユーザーは、LCS の組織のワークスペースに自動的にアクセスし、参加するように招待されたすべてのプロジェクトを表示できます。 CustomerSource および PartnerSource の組織の管理者になっているユーザーは LCS の管理者になります。 <br>

管理者は CustomerSource または PartnerSource の資格情報を持っていないユーザーを LCS の組織のメンバーに招待できますが、この方法はお勧めしません。 LCS 組織のメンバーとなるよう招待されたユーザーには、CustomerSource または PartnerSource での資格情報が提供されません。 <br> 

LCS へのプロジェクト レベル アクセスは、招待によって行われます。 プロジェクトの所有者およびチーム メンバーとして組織のメンバーを招待することができます。 また、組織のメンバーではなく、Azure AD、CustomerSource、または PartnerSource のアカンウントを持たないユーザーをチーム メンバーに招待できます。

> [!IMPORTANT]
> 会社内のすべてのユーザーを組織レベルで管理することを強くお勧めします。 この方法で、組織との関係が CustomerSource、PartnerSource、および Azure AD で正しいことを確認できます。 また、ユーザーが組織で利用できる福利厚生にアクセスできることを確認します。

## <a name="manage-lcs-organization-users"></a>LCS 組織のユーザーの管理
管理者のみユーザーを管理できます。 以下の手順を実行します。

1.  CustomerSource、PartnerSource、または Azure AD で、LCS へのアクセスを必要とする組織内のすべてのユーザーを組織と関連付けます。 ユーザーは、LCS にログインできるようになるまでに、2 営業日待機することが必要な場合があります。
2.  LCS の適切なプロジェクトに、ユーザーを追加します。

### <a name="invite-a-user-to-an-lcs-project"></a>LCS プロジェクトへのユーザーの招待

1.  [LCS](https://lcs.dynamics.com/) にサインインします。
2.  プロジェクトを選択してユーザーを追加します。
3.  **プロジェクト ユーザー** タイルを選択し、**プロジェクト ユーザー** ページで、プラス記号 (**+**) を選択します。
4.  ユーザーの電子メール アドレスを入力し、次に正しいセキュリティ ロールを選択して、**招待** を選択します。

> [!NOTE]
> 実装プロジェクトで、招待されたユーザーの実装ロールを選択できます。 **FastTrack からの連絡を許可する** を **はい** に設定した場合、Microsoft FastTrack チームは実装ロールと実装プロジェクトのステージに基づいてご連絡を差し上げる場合があります。   

## <a name="working-with-customersource-and-partnersource"></a>CustomerSource および PartnerSource での作業
このセクションの情報は、CustomerSource または PartnerSource へのアクセスを支援することを目的としています。

### <a name="signing-in-to-customersource-or-partnersource"></a>CustomerSource または PartnerSource へのサインイン

[CustomerSource サインイン ページ](https://docs.microsoft.com/dynamics/s-e/)に移動し、Microsoft アカウント (以前は Windows Live ID と呼ばれる) のユーザー名とパスワードを入力してサイトにアクセスします。 組織の CustomerSource 勘定へのアクセスがない場合、「[CustomerSource](https://docs.microsoft.com/dynamics/s-e/northamerica/news-events/news-events/news/NeedAccesstoCustomerSource) にログインする方法」ページに従います。

### <a name="determining-the-administrator-for-your-organization-in-customersource-or-partnersource"></a>CustomerSource または PartnerSource で組織の管理者を決定する

CustomerSource の管理者がわからない場合、または組織に CustomerSource 管理者がいない場合は、電子メールを [itmbssup@microsoft.com](mailto:itmbssup@microsoft.com) に送信してお問い合わせください。

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
実装プロジェクトがある場合、プロジェクト ユーザーの実装ロールを指定するためのオプションが表示されます。 詳細については、[Dynamics 365 実装のロール](https://docs.microsoft.com/learn/modules/get-started-implementation-project/01-2-roles) を参照してください。




[!INCLUDE[footer-include](../../../includes/footer-banner.md)]